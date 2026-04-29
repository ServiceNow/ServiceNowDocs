---
title: All other Australia fixes
description: The Australia release contains important problem fixes.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 144
breadcrumb: [Available patches and hotfixes, Learn about the Australia release, Australia release notes]
---

# All other Australia fixes

The Australia release contains important problem fixes.

-   **Australia was released on March 12, 2026.**
    -   03-04-2026\_1355
    -   glide-australia-02-11-2026\_\_patch0-02-24-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This version is being evaluated for use in the ServiceNow Government Community Cloud \(GCC\) environment.

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/australia/rn/patches/PRBs-A00.00.xlsx)

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

PRB1966968

</td><td>

ScriptingGovernanceUtils does not correctly create sys\_user\_has\_role records for the snc\_required\_script\_writer\_permission based on the legacy/V1 or V2 Role Management mechanisms

</td></tr><tr><td>

Access Control

</td><td>

PRB1928472

</td><td>

Unable to assign a 'Customer' admin role to a contact from the contact view page from CSM portal

</td></tr><tr><td>

Access Control

</td><td>

PRB1913056

</td><td>

Query range ACL can be created with script

</td></tr><tr><td>

Access Control

</td><td>

PRB1813550

</td><td>

Files are missing during upgrade of plugin

</td></tr><tr><td>

Access Control

</td><td>

PRB1928139

</td><td>

Field-level ACLs on database views appear to behave differently between .\* and specific field names

</td></tr><tr><td>

Access Control

</td><td>

PRB1933758

</td><td>

Read allow ACLs are skipped evaluation

</td></tr><tr><td>

Access Control

</td><td>

PRB1936192

</td><td>

The Security Constraints error message is not getting displayed on the new record if a user does not have create access

</td></tr><tr><td>

Access Control

</td><td>

PRB1938078

</td><td>

Excessive syslog logging from AccessTerm "Slow ACL"

</td></tr><tr><td>

Access Control

</td><td>

PRB1949281

</td><td>

The 'Scripting Governance Tool' documentation link isn't working

</td></tr><tr><td>

Access Control

</td><td>

PRB1959231

</td><td>

The QueryRangeACLAuditor script needs always print the final log statement on line 5981

</td></tr><tr><td>

Access Control

</td><td>

PRB1892720

</td><td>

'Applies to' in the Deny Unless Read ACL doesn't work for users with elevated privileges

</td></tr><tr><td>

Access Control

</td><td>

PRB1914077

</td><td>

The Description field on ACL is not updating correctly

</td></tr><tr><td>

Access Control

</td><td>

PRB1919311

</td><td>

AddEncodedQuery in "Case Query rules" Business Rule is trying to get results using an invalid query

</td></tr><tr><td>

Access Control

</td><td>

PRB1930955

</td><td>

While updating the list records using 'Update All', the list context menu throws an error

</td></tr><tr><td>

Access Control List \(ACL\) Rules

</td><td>

PRB1918943

</td><td>

Ensures QueryRangeACLAuditor rerun to preserve the timestamps of query ACLs created by previous audit run

</td></tr><tr><td>

Access Control List \(ACL\) Rules

</td><td>

PRB1964011

</td><td>

AllTermsCache has an increased live set of close to 20 MB in Zurich

</td></tr><tr><td>

Action Bar Component

</td><td>

PRB1754460

</td><td>

UI Action Bar moves downwards when resizing the window in the Service Operations Workspace

</td></tr><tr><td>

Action Bar Component

</td><td>

PRB1865188

</td><td>

The 'Approval' and 'Reject' buttons are shown twice for a delegated user on approval records or problem

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1936699

</td><td>

Activity stream flickers when the work notes are in modless view

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1973866

</td><td>

When showEmailMiniCompose = ON\_EMAIL\_ACTION, users can't reply to an email more than once

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1972203

</td><td>

@mention menu pop-up in workspace appears when removing trailing whitespace

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1890722

</td><td>

Attachment details are displayed incorrectly in the workspace activity stream when attaching a duplicate attachment to an email

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1894503

</td><td>

Typing and posting a comment rapidly can result in missing characters

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1923171

</td><td>

When the Journal field is truncated, new lines are lost

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1854197

</td><td>

Create a configurable sys property for a search's duration when searching for emails related to new records

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1743672

</td><td>

Work notes using a carriage return aren't displaying in HR Agent Workspace when using Edge encryption

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1959209

</td><td>

Paragraph spacing is lost after editing and saving a long post in the plain text editor

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1936307

</td><td>

@mention in journal input doesn't appropriately respond to assistive technologies

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1954291

</td><td>

An attachment with no creation date causes a null point error and the activity stream doesn't render on UI16

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1969041

</td><td>

Focus remains on the 'Email' tab after 'Save'

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1972588

</td><td>

Dependency fields are not resolved if the dependent field is not part of the filter

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1868703

</td><td>

Slow queries against the sharded sys\_audit table when populating the Activity Stream

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1899572

</td><td>

The Activity section of the Details tab doesn't show field changes upon incident creation

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1926219

</td><td>

Assignment rule is shown as updated by user name instead of system post Washington in the activity stream

</td></tr><tr><td>

Adaptive Authentication

</td><td>

PRB1902875

</td><td>

Adaptive Auth idenityProvider filter doesn't result in null

</td></tr><tr><td>

Adaptive Authentication

</td><td>

PRB1945533

</td><td>

Users are able to register a mobile device with an expired QR code in 'Trusted mobile device'

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1943775

</td><td>

Walk-up interaction state is restricted by HR scope ACLs

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1914068

</td><td>

The executeTimeoutJob from Advanced Work Assignment \(AWA\) might be attempting it again and going into a loop, blocking the node to come up

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1932373

</td><td>

'Block relationship autocreation' business rule logic was not fixed correctly

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1933671

</td><td>

AWA \(Advanced Work Assignment\) uses the system locale timezone when writing to logs

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1939743

</td><td>

Interaction and AWA Interaction Work Item records show different assignment/wait time values

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1944387

</td><td>

The 'Create Segment On WorkItem Accept' business rule runs unnecessarily when a previous accepted work item exists

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1950553

</td><td>

Interaction list is taking time

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1950970

</td><td>

Re-opening an alert triggered after agents manually mark a chat as 'closed abandoned' should be prevented

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1959522

</td><td>

Agents are able to send messages even after a conversation is closed

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1965535

</td><td>

MessagingActionUtils doesn't handle exceptions when sending messages, breaks messaging action timers

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1975706

</td><td>

Standby node takes 1.5 hours to launch online

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1982818

</td><td>

After removing a service channel, the current universal capacity of the agent isn't decreased

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1874401

</td><td>

The awa\_queue\_trigger translation is not reflect in the agent chat when the language is set to French

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1900404

</td><td>

Delay between poke and routing caused by the assigner thread not running on UI nodes

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1918004

</td><td>

The configuration on Assignment eligibility - Eligible At is not reflected on Agent Chat

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1929089

</td><td>

Missing index on awa\_work\_item \(state, claimed\_for, executed\_by\)

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1929864

</td><td>

The chat card remains in the agent inbox after the guest ends the conversation

</td></tr><tr><td>

Agent Assist

</td><td>

PRB1918072

</td><td>

Similarity Definition is not working

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1935719

</td><td>

Chat opens for closed, complete interactions in the configurable workspace

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1964909

</td><td>

When an agent receives a new interaction within the workspace, the non-focused tab won't blink or flash

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1922878

</td><td>

The agent chat's audio alert for inbox should stop playing when the agent has responded even if the alert's mp3 has not finished playing

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1939251

</td><td>

Agent chat dynamic translation doesn't work as expected on per chat basis

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1960915

</td><td>

Live Chat Messages from Agents are not appearing in the end user UI

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1937850

</td><td>

Agents are unable to view messages sent by end users that contain URLs formatted with an HTML &lt;a&gt; tag when DTAC is enabled

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1943203

</td><td>

When hovering through the response templates, the preview is obstructed/hidden behind the case form

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1943902

</td><td>

Create a new exclusive channel to receive work items on Agent Chat

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1957261

</td><td>

Invoke end chat summarization in a 'system' topic

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1959396

</td><td>

AWA workitemResponder onChange published message causes a work item card to disappear in the workspace

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1970805

</td><td>

After transferring the chat to another queue, the previous agent is still able to send chats on the transferred interaction

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1979795

</td><td>

Users can't update the agent chat status message content consistently via \[sys\_ui\_message\] records

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1982490

</td><td>

RECORD\#OPEN\_CALL event isn't emitted during manual reject for transferred work items

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1836368

</td><td>

Desktop message notification with unwanted content is triggered after an asynchronous chat ends

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1908263

</td><td>

Safari audio issues in inactive tabs

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1921738

</td><td>

Survey questions do not appear in the Active Chat window for Agent

</td></tr><tr><td>

Agent Inbox

</td><td>

PRB1972409

</td><td>

Incorrect Quick Action filtering when THIRD\_PARTY\_INTEGRATION is missing or disabled

</td></tr><tr><td>

Agile Development

</td><td>

PRB1968771

</td><td>

/sn\_safe\_$safe\_board.do\#/teamBacklog is broken

</td></tr><tr><td>

Agile Development

</td><td>

PRB1905318

</td><td>

Base instance process flow formatter for table doesn't match with the flow

</td></tr><tr><td>

AI Agents \(Glide Family\)

</td><td>

PRB1972747

</td><td>

Ten assists for catalog execution in the fully agentic should be charged

</td></tr><tr><td>

AI Search

</td><td>

PRB1931645

</td><td>

AI Search listens to events such as 'sys\_cache\_flush' and can cause stack overflow exceptions

</td></tr><tr><td>

AI Search

</td><td>

PRB1896807

</td><td>

'Index All Table' from the list view of a datasource should trigger 'No block indexing' instead of 'Block reindexing'

</td></tr><tr><td>

AI Search

</td><td>

PRB1745417

</td><td>

User with 'ais\_high\_security\_admin' role doesn't get any search results

</td></tr><tr><td>

AI Search

</td><td>

PRB1887375

</td><td>

'OR' conditions aren't correctly evaluated in EVAM lite

</td></tr><tr><td>

AI Search

</td><td>

PRB1861012

</td><td>

Sn-search-combobox sends exact match data broker execution

</td></tr><tr><td>

AI Search

</td><td>

PRB1892424

</td><td>

In AI Search, there's an incorrectly wrapped string in t\(\) function

</td></tr><tr><td>

AI Search

</td><td>

PRB1829924

</td><td>

On the Next Experience global search, 'Recently viewed' doesn't display an incident number and only displays text in the subdomain

</td></tr><tr><td>

AI Search

</td><td>

PRB1902960

</td><td>

Now Assist Q&amp;A Genius Results don't display when the Log Signals Server side is turned on through Search Application Configuration

</td></tr><tr><td>

AI Search

</td><td>

PRB1949749

</td><td>

AI Search doesn't return results on the latest znowassist instances

</td></tr><tr><td>

AI Search

</td><td>

PRB1962777

</td><td>

NBA/RAG doesn't use applicable\_skills

</td></tr><tr><td>

AI Search

</td><td>

PRB1780159

</td><td>

An AI Search pop-up with 'Recently Viewed:' and 'Suggested' groupings aren't identified to assistive technology users

</td></tr><tr><td>

AI Search

</td><td>

PRB1819970

</td><td>

The Knowledge Article view count is not incremented by attachment download in AI Search

</td></tr><tr><td>

AI Search

</td><td>

PRB1820525

</td><td>

The full\_text chunking format is not indexing or querying the entire document

</td></tr><tr><td>

AI Search

</td><td>

PRB1830825

</td><td>

Taxonomy topic field on the sc\_cat\_item indexed source is not ingested due to an SQL exception in a domain separated and multi-lingual glide environment

</td></tr><tr><td>

AI Search

</td><td>

PRB1894396

</td><td>

Linking a new source profile does not mark the target profile's state as 'DRAFT'

</td></tr><tr><td>

AI Search

</td><td>

PRB1895430

</td><td>

SPSearchResultActions client callable scriptable is not available to unauthenticated users

</td></tr><tr><td>

AI Search

</td><td>

PRB1897733

</td><td>

When an attachment upload fails, all documents in the batch are not indexed

</td></tr><tr><td>

AI Search

</td><td>

PRB1907730

</td><td>

Global search icon color with zing for theming

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1936969

</td><td>

Spinner or loader is still shown when Genius Result \(GR\) isn't linked to the search application

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1897038

</td><td>

There are too many errors when AisRelevancyService doesn't have enough signals to train ML solution

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1944944

</td><td>

RAG corrupted AI Search results sends back the wrong sys\_id and text in results

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1930534

</td><td>

When used on service portals, 'Exact Match' should honor search sources

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1971388

</td><td>

IngestableDocument.getObjectSize isn't counting fEmbeddedDocuments

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1972570

</td><td>

displayValue in location gives the sysID rather than the country code

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1921724

</td><td>

Improve ResponsePostProcessor time when the table is early binding

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1939064

</td><td>

Malformed field "is\_conversational" in AIS response

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1939319

</td><td>

When the user first navigates to Full page search and executes a search on chat, an empty search databroker is executed

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1954965

</td><td>

The 'Query Timeout' property doesn't configure application level timeout

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1961490

</td><td>

The user cannot ingest semantic fields for skills in a non-global domain

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1990134

</td><td>

If all KBBs from one doc are removed from KB late binding, the post process stops and all following docs are returned

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1914943

</td><td>

Child catalog item e.g. sc\_cat\_item\_guide is re-indexed incorrectly to sc\_cat\_item after record is inserted to sc\_cat\_item\_category

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1916606

</td><td>

The User Context "Country" uses a display value instead of a country code but ais\_rule.trigger uses country\_code

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1921293

</td><td>

The Glide List field is indexed only in English during full ingestion despite non-English KB language

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1926964

</td><td>

E5 encoding does not work when a non-base instance English \(EN\) record is created in the sys\_language table

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1931346

</td><td>

KB Article rendering issues in Agent Chat

</td></tr><tr><td>

AI Search Assist

</td><td>

PRB1928988

</td><td>

'Invalid Date' is displayed in the 'Last Modified' field in the AI Search Assist Widget

</td></tr><tr><td>

AI Search Assist

</td><td>

PRB1956754

</td><td>

The AI Search results expand/collapse chevron has no accessibility mark-up, causing it to not exist for screen reader users and keyboard-only users

</td></tr><tr><td>

AI Search for Service Portal

</td><td>

PRB1956814

</td><td>

Pressing the 'Enter' key doesn't open the link

</td></tr><tr><td>

AI Search for Virtual Agent

</td><td>

PRB1831062

</td><td>

For the Virtual Agent in the Employee Center, 'Here's what I found for \{0\}' appears as hardcoded

</td></tr><tr><td>

AI Search for Virtual Agent

</td><td>

PRB1932162

</td><td>

Marking KG 'None' in the Conversational Interface invokes the 'Text To Result' call

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1946473

</td><td>

The enhanced search typeahead widget doesn't honor the placeholder value

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1980290

</td><td>

In the Service Portal with Now Assist enabled, when the tab focus is on the link and the 'Enter' key is pressed, the link doesn't open

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1963505

</td><td>

URLs towards the end of the streaming are rendered as plain text

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1923669

</td><td>

Citations rendered as raw JSON when async/streaming is disabled

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1956521

</td><td>

Results whose titles start with an @ and contain &lt;/highlight&gt; \(due to hit highlighting\) don't render correctly

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1768030

</td><td>

Search function duplicated details are read out within search results

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1935102

</td><td>

AI Search Search Source Preview Link does not correctly handle "New Conditions"

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1951137

</td><td>

Don't pass a Virtual Agent Entity View Action Mapper \(EVAM\) ID when enhanced chat isn't turned on

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1957805

</td><td>

A sparkle icon color can't be set during animation

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1962691

</td><td>

AI Search doesn't populate sys\_search\_source\_event with sources that weren't returned

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1963984

</td><td>

Streaming fails when there's a response with numerous citations

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1977757

</td><td>

Portal search loses search\_results\_configuration context when resubmitting search

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1920766

</td><td>

For Search Signals, kb\_knowledge citations do not log tables in sys\_search\_signal\_event

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1928007

</td><td>

An empty GR result is shown when a multi-content GR response is returned for a different search

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1928306

</td><td>

"Filter Genius Results by tab" configuration on Search Application form is not respected in portal search

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1930672

</td><td>

A Service Portal Genius Result \(GR\) synthesized response flashes and changes text size

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1932120

</td><td>

Non-conversational catalogs shouldn't have an option to request in a chat

</td></tr><tr><td>

AI Service - Glide Interfaces

</td><td>

PRB1919181

</td><td>

The 'Ml solution' table gets updated whenever a prediction is done because of the 'last accessed time' column

</td></tr><tr><td>

Alert Aggregation

</td><td>

PRB1947502

</td><td>

Improve logging in the 'Service Analytics - Update virtual alerts for aggregation groups' logic

</td></tr><tr><td>

Analytics and Reporting Solutions for Service Portal

</td><td>

PRB1976877

</td><td>

Focus order issue in Open Analytics Window

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1931476

</td><td>

Issue with Incident SLA donut translation in Service Operations Workspace \(SOW\)

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1894963

</td><td>

Data Visualization drilldown doesn't follow previous filters

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1944148

</td><td>

PAE real-time isn't possible when the breakdown filter includes a scripted mapping for a different table

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1928857

</td><td>

The maximum number of groups on the heat map visualization in Platform Analytics resets to 10 when filtering

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1937286

</td><td>

When a visualization acts as filter, another visualization isn't filtered for the first time

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1956708

</td><td>

In Platform Analytics, there's an issue with time series visualization when grouped by breakdown

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1962112

</td><td>

Time series with 'Group by' elements in report range doesn't display the correct data

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1967291

</td><td>

After an upgrade, Platform Analytics reports and dashboards aren't able to viewed by users

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1980107

</td><td>

In Platform Analytics's Data Visualizations's 'Trend By', there's no support to select calendar\_date\_time fields

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1986630

</td><td>

Domain isn't included while generating a key for the indicator data source

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1892623

</td><td>

Data visualization on a pivot table shows 0 or incorrect/inconsistent data

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1897544

</td><td>

Chart interaction fails in Bubble Data Visualization when using a decimal-type field configured via dot-Walk \(Reference field\) under Xanadu and Yokohama dimensions

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1904385

</td><td>

PAR Bar chart sorting does not work if multiple visualizations have same data source filters, 'group by' and max number of groups in a dashboard or tab

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1914015

</td><td>

Data is not populated for Ratings widgets

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1915499

</td><td>

The funnel is displayed incorrectly in the workload saving widget

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1926216

</td><td>

Add proper support for different variable types

</td></tr><tr><td>

Analytics Hub

</td><td>

PRB1930155

</td><td>

Comments created date inside a widget display the wrong created date

</td></tr><tr><td>

Anonymous Report Center \(ARC\)

</td><td>

PRB1736778

</td><td>

Pop-up message reloads when an employee enters the Anonymous Report Center

</td></tr><tr><td>

Anonymous Report Center \(ARC\)

</td><td>

PRB1931937

</td><td>

Anonymous report PDF displaying sys ID instead of display name

</td></tr><tr><td>

API Access Policies

</td><td>

PRB1940494

</td><td>

The post-authentication policy from one CBA or WSSE overwrites the outcome of other policies with the same type

</td></tr><tr><td>

API Access Policies

</td><td>

PRB1917216

</td><td>

Authenticate header for browser redirect to API is Basic when logged in

</td></tr><tr><td>

App Engine Studio - Family Channel

</td><td>

PRB1906919

</td><td>

Flow created from App template does not have trigger configured

</td></tr><tr><td>

App Engine Studio - Family Channel

</td><td>

PRB1923756

</td><td>

The Record Producer remains as the original template's one in a newly created app

</td></tr><tr><td>

Application Collaboration

</td><td>

PRB1833256

</td><td>

Delegated developers can see installed applications in 'My Company Applications'

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1930608

</td><td>

After a migration job was successfully completed, the glide property is not updated

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1914695

</td><td>

If the soft dependency version is not available, the entire app installation fails

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1925437

</td><td>

The Installation Logs related list does not show any logs for the global app

</td></tr><tr><td>

Application Manager

</td><td>

PRB1963964

</td><td>

The install/update modal for any Now Assist app that loads the new Now Assist suite UX takes over two minutes to load

</td></tr><tr><td>

Application Manager

</td><td>

PRB1945557

</td><td>

A Vulnerability Response application fails to load due to a long-running query in the AppsData script include

</td></tr><tr><td>

Application Manager

</td><td>

PRB1964007

</td><td>

Sys\_prop is polluting the update set

</td></tr><tr><td>

Application Manager

</td><td>

PRB1920459

</td><td>

Nodes aren't coming online, and java.lang.Class CastException in the wrapper logs a boot

</td></tr><tr><td>

Application Manager

</td><td>

PRB1618401

</td><td>

sn\_impex.GlideImportSetTransformMap\(\) script doesn't work as expected in cross scope

</td></tr><tr><td>

Application Manager

</td><td>

PRB1872434

</td><td>

Apps are not listed under 'Products' during offline upload

</td></tr><tr><td>

Application Manager

</td><td>

PRB1888295

</td><td>

Unable to open the 'Product details' page with apps after uploading a .store file

</td></tr><tr><td>

Application Manager

</td><td>

PRB1895645

</td><td>

The script call 'new UpdateChecker\(\).checkAvailableUpdates\(\);' creates an extra sys\_update\_version record

</td></tr><tr><td>

Application Manager

</td><td>

PRB1926354

</td><td>

Not Licensed applications are showing up under the Licensed list for the Service Operations Workspace product in Application manager

</td></tr><tr><td>

Application Rationalization

</td><td>

PRB1942817

</td><td>

Issues with the 'Dependency' view in Enterprise Architecture Workspace

</td></tr><tr><td>

Application Rationalization

</td><td>

PRB1945947

</td><td>

Deletion of a TRM product doesn't delete the associate lifecycle record

</td></tr><tr><td>

Appointment Booking

</td><td>

PRB1958490

</td><td>

The 'Reschedule' UI action isn't displaying any appointments

</td></tr><tr><td>

Appointment Booking

</td><td>

PRB1973793

</td><td>

Blackout schedule isn't honored

</td></tr><tr><td>

Appointment Booking

</td><td>

PRB1922446

</td><td>

The error "Function log is not allowed in scope sn\_apptmnt\_booking. Use gs.debug\(\) or gs.info\(\) instead" occurrs when upgrading Yokohama

</td></tr><tr><td>

Appointment Booking

</td><td>

PRB1923326

</td><td>

There's insufficient server-side input validation for 'Reschedule Appointment' in FSM appointment booking

</td></tr><tr><td>

Appointment Booking

</td><td>

PRB1925169

</td><td>

The 'Book Appointment' Dialog Box is not automatically closed and the 'Reschedule Appointment' title is showing for a first time booking

</td></tr><tr><td>

Approvals

</td><td>

PRB1900608

</td><td>

The approval history entries 'added as an approver' are duplicated on record

</td></tr><tr><td>

Approvals

</td><td>

PRB1928314

</td><td>

Re-triggered change approvals aren't routing to the user who rejected them previously

</td></tr><tr><td>

Approvals

</td><td>

PRB1965496

</td><td>

Add approval delegation helper methods to retrieve only requested approvals and help improve performance in Service Portal

</td></tr><tr><td>

Approvals

</td><td>

PRB1840427

</td><td>

Approval record history access is blocked when the state is 'No longer required'

</td></tr><tr><td>

Approvals

</td><td>

PRB1914382

</td><td>

When a change is accepted or rejected, a work note message is not translated

</td></tr><tr><td>

Approval with E-signature

</td><td>

PRB1955867

</td><td>

'Approval reason' field should be empty when no reason is provided

</td></tr><tr><td>

Approval with E-signature

</td><td>

PRB1962541

</td><td>

In workspace, an eSig popup doesn't appear when using the inline approval

</td></tr><tr><td>

Archive Rules

</td><td>

PRB1898325

</td><td>

In the 'Archive Rule' form in 'Archive Related Records' tab, a related record can point or reference the main archive rule in the 'Reference Table Rule' field

</td></tr><tr><td>

Archive Rules

</td><td>

PRB1931605

</td><td>

"retain\_references" flag should be inherited from an archive rule on the parent table instead of defaulting it to false when there is no archive rule for the table

</td></tr><tr><td>

Assessments

</td><td>

PRB1902714

</td><td>

When a scripted method assessment metric is used, the normalised value calculation is different

</td></tr><tr><td>

Asset Management

</td><td>

PRB1964198

</td><td>

Model business rule 'Update asset display names' times out transactions due to synchronous bulk updates on assets

</td></tr><tr><td>

Asset Management

</td><td>

PRB1948574

</td><td>

Baseline insert, insert, and stay functionalities in Asset Management are broken because of incorrect PID implementation

</td></tr><tr><td>

Asset Management

</td><td>

PRB1942227

</td><td>

Users are unable to create certain asset types in Asset Workspace in Japanese

</td></tr><tr><td>

Asset Management

</td><td>

PRB1943052

</td><td>

A sys\_update\_xml record isn't created when updating a translation

</td></tr><tr><td>

Asset Management

</td><td>

PRB1953435

</td><td>

The heading structure is incorrect for an Asset Workspace homepage

</td></tr><tr><td>

Asset Management

</td><td>

PRB1964071

</td><td>

The bulk update of a UI action generates a warning message when selecting 'Received'

</td></tr><tr><td>

Asset Management

</td><td>

PRB1968544

</td><td>

Assets which were created aren't displaying in 'Create Asset' on the Agent Mobile app

</td></tr><tr><td>

Asset Management

</td><td>

PRB1973670

</td><td>

Transfer order tasks are cancelled, but the active flag remains turned on

</td></tr><tr><td>

Asset Management

</td><td>

PRB1976533

</td><td>

The Asset Creation queue uses a user session domain instead of a CI domain

</td></tr><tr><td>

Asset Management

</td><td>

PRB1903399

</td><td>

When a pre-allocated value is selected for substate, both state and substate become read-only

</td></tr><tr><td>

Asset Management

</td><td>

PRB1915546

</td><td>

Empty terms and condition records are created if the user tries to update terms and condition while trying to create a contract

</td></tr><tr><td>

Asset Management

</td><td>

PRB1923537

</td><td>

Default view for Hardware Models table not showing in Views list

</td></tr><tr><td>

Asset Management

</td><td>

PRB1926850

</td><td>

Mismatched units in model form

</td></tr><tr><td>

Asynchronous Message Bus \(AMB\)

</td><td>

PRB1940517

</td><td>

Improvise performance of AMBQuickMessageDeliverer thread by using a shared lock when polling from two queues repeatedly

</td></tr><tr><td>

Asynchronous Message Bus \(AMB\)

</td><td>

PRB1906536

</td><td>

Asynchronous Message Bus \(AMB\) publishes calls through PubSub and fails for Record Watcher and VTB use cases

</td></tr><tr><td>

Attachments to Records

</td><td>

PRB1920687

</td><td>

User can see the 'New' and 'Edit' buttons in attachment attribute table

</td></tr><tr><td>

Attachments to Records

</td><td>

PRB1952615

</td><td>

Can't upload big files after upgrade to Zurich

</td></tr><tr><td>

Attachments to Records

</td><td>

PRB1857893

</td><td>

Attachment upload modal window shows null when an attachment with an empty file name is present in the sys\_attachment table

</td></tr><tr><td>

Attachments to Records

</td><td>

PRB1977787

</td><td>

Adding the prefix 'ZZ\_YY' hides all references to an attachment in a record

</td></tr><tr><td>

Attachments to Records

</td><td>

PRB1954868

</td><td>

The 'Delete' option is visible in the 'Attachment' section in workspace even after restricting the access to delete attachments in the Zurich version

</td></tr><tr><td>

Attachments to Records

</td><td>

PRB1879578

</td><td>

New button on the Attachment related list opens a a sys\_attachment form when it should not, and when submitted, it adds a zero byte attachment to the Activity Stream with no content type

</td></tr><tr><td>

Attachments to Records

</td><td>

PRB1916743

</td><td>

Cannot update Virtual Agent chat notification sound

</td></tr><tr><td>

Audit History

</td><td>

PRB1958048

</td><td>

Audit TTL job doesn't clear the data from sys\_audit on extension shards

</td></tr><tr><td>

Audit History

</td><td>

PRB1933089

</td><td>

The user is unable to see 'History &gt; List ' on the form when the ACL is created with 'Applied to' or 'Data Condition'

</td></tr><tr><td>

Audit History

</td><td>

PRB1928527

</td><td>

Handling of NPE in historyWalker due to unknown fields appearing even they are not part of table's columns

</td></tr><tr><td>

Audit History

</td><td>

PRB1931990

</td><td>

Logs flowin to the active sys\_audit sharded table

</td></tr><tr><td>

Authentication

</td><td>

PRB1913258

</td><td>

In the IP Filter Criteria Record, the user can't add a description to an existing range

</td></tr><tr><td>

Authentication

</td><td>

PRB1891591

</td><td>

Customer workflow triggered from last\_login\_time updates can cause the ACL result to be cached as guest in transaction

</td></tr><tr><td>

Authentication

</td><td>

PRB1975818

</td><td>

The property glide.authenticate.failed\_redirect is not working after login failure

</td></tr><tr><td>

Authentication

</td><td>

PRB1897600

</td><td>

Log mutual authentication errors in AuthnLog for Dev Crypto API calls using mutual authentication

</td></tr><tr><td>

Authentication

</td><td>

PRB1901442

</td><td>

Mismatch in failed login attempts for sys\_event and Security Center Records

</td></tr><tr><td>

Authentication

</td><td>

PRB1918178

</td><td>

Insufficient Non-Text Contrast for Response Time \(Stopwatch\) icon button on the login page

</td></tr><tr><td>

Authentication

</td><td>

PRB1920095

</td><td>

A long "Change Password" UI Message causes formatting issues on the Next Experience version of Change Password Page \(login\_cpw.do\)

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1932771

</td><td>

An ATF step UI Action visibility fails to find a UI action when sys\_ui\_action.client = true

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1943666

</td><td>

The ATF Page Inspector component list is empty on portal pages with AI Search turned on

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1900456

</td><td>

Set the sys\_trigger state with a recognizable or meaningful state instead of state -1776

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1937603

</td><td>

'Copy Test' for Reusable Tests does not copy reusable input/output variables

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1920825

</td><td>

ATF becomes less responsive if a large number of cloud runner tests are queued

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1933246

</td><td>

ATF does not select exact match in select2 component when there is more than one selection available

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1941169

</td><td>

ATF reusable test input/output variables do not have a default form layout

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1956099

</td><td>

'Add Test Step' modal is blank for atf\_test\_admin users after installing the Cloud Account Management app

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1966193

</td><td>

The accessibility label of a file attachment is hardcoded

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1892104

</td><td>

Automated Test Framework \(ATF\) returns''\[object Object\]'' error in 'Module Visibility' step when testing Next Experience UI

</td></tr><tr><td>

Auto Resolution Simulation

</td><td>

PRB1843989

</td><td>

Issue with the extraction of the term 'Delete' in the platform sys\_ui\_message for Yokohama

</td></tr><tr><td>

Batch API

</td><td>

PRB1911987

</td><td>

Search sources in UI Builder 's Source to Pay workspace Experience setting is null

</td></tr><tr><td>

Cache

</td><td>

PRB1953827

</td><td>

There's errors in the system/error log since Zurich

</td></tr><tr><td>

Cache

</td><td>

PRB1922845

</td><td>

File handlers are left open if a LazyInputStream is closed before being read by LargeContentDiskCache

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1933229

</td><td>

Incorrect UI policy causing issues on 'View Responses' UI action for sn\_hr\_core\_task

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1935669

</td><td>

hr\_SecurityUtils.getCoeSecurityPolicy script include API may error when the 'Services' field is empty

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1899272

</td><td>

HR uptake on scope mastering on sys\_email, asmt\_assessment\_instance, and sysapproval\_approver

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1960734

</td><td>

HR templates with scripts aren't working after upgrading to Zurich

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1946786

</td><td>

A primary job isn't set for an alumni record

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1981562

</td><td>

Transferring an HR case in the 'Ready' state to a new 'Service activity' fulfillment type HR case does not create approval records

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1891255

</td><td>

Agent unable to add a tag in a HR case

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1895171

</td><td>

Job code is updated in the sys\_user record when the sn\_hr\_core\_job record has been updated

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1901297

</td><td>

HR Task Widget is not formatting the Description as HTML

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1920799

</td><td>

'Preview document' functionality on PDF displays '&amp;' incorrectly

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1922313

</td><td>

Synchronization of Phone Field from User Record to HR Profile only during record creation, but not during updates

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1924244

</td><td>

Duplicate constant "TASK\_IN\_PROGRESS" in Script Include "sn\_hr\_core.hr\_Constants"

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1924672

</td><td>

Retiring a knowledge block results in a blank confirmation dialog

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1926747

</td><td>

The vendor portal take-questionnaire page stops working when an HR application is installed

</td></tr><tr><td>

Case Management

</td><td>

PRB1922249

</td><td>

Async business rule 'Set First Contact Resolution' updates the case status to a stale value

</td></tr><tr><td>

Case Management

</td><td>

PRB1926739

</td><td>

The user is not able to access an overview link from a customer service module

</td></tr><tr><td>

Case Management

</td><td>

PRB1934610

</td><td>

HistoryWalker code in base instance action 'Check if comment is added by others' throws errors

</td></tr><tr><td>

Case Management

</td><td>

PRB1952952

</td><td>

A non-admin is unable to save 'Applies to' in the special handling notes

</td></tr><tr><td>

Case Management

</td><td>

PRB1965548

</td><td>

The 'Entitlement' field of cases isn't populated when a language pack is installed

</td></tr><tr><td>

Case Management

</td><td>

PRB1863306

</td><td>

Metric definition script is not validating results, causing log errors downstream

</td></tr><tr><td>

Case Management

</td><td>

PRB1863313

</td><td>

Metric Definition script is not validating results, causing log errors downstream with messages indicating 'String contains contol character'

</td></tr><tr><td>

Catalog Portal Pages

</td><td>

PRB1847275

</td><td>

Session messages are not shown if the current action is aborted by business rules

</td></tr><tr><td>

Catalog UI Policies

</td><td>

PRB1913676

</td><td>

'Reverse if false' isn't honored when the UI policy is triggered from VA

</td></tr><tr><td>

Change Management

</td><td>

PRB1931749

</td><td>

The 'Impact' field isn't updated after running risk calculation

</td></tr><tr><td>

Change Management

</td><td>

PRB1953175

</td><td>

The 'Notify assessment' user notification is triggered unnecessarily for change risk assessments

</td></tr><tr><td>

Change Management

</td><td>

PRB1893090

</td><td>

Slow processing of 'change\_request.trigger.discovery' due to slow Discovery API calls

</td></tr><tr><td>

Change Management

</td><td>

PRB1983792

</td><td>

Different users triggering change risk assessments without completing them get a security error

</td></tr><tr><td>

Change Management

</td><td>

PRB1932643

</td><td>

There are English messages in the activity log for change requests

</td></tr><tr><td>

Change Management

</td><td>

PRB1946871

</td><td>

A user with a new role added to the 'change.conflict.role' system property gets a security constraint, preventing access to a requested page when checking conflicts

</td></tr><tr><td>

Change Management

</td><td>

PRB1950401

</td><td>

Duplicate approvals are created when a proposal is approved for retiring the standard change template

</td></tr><tr><td>

Change Management

</td><td>

PRB1974660

</td><td>

If the user checks conflicts before saving a child change from project RITM, the CHG won't be attached to the parent RITM

</td></tr><tr><td>

Change Management

</td><td>

PRB1981054

</td><td>

For change models, the 'Reusables' client script forces type to 'normal' if the type isn't included in the presets

</td></tr><tr><td>

Change Management

</td><td>

PRB1906840

</td><td>

Inconsistent hover text behavior on models in the Change Management landing page

</td></tr><tr><td>

Change Management

</td><td>

PRB1911948

</td><td>

Rejecting the Standard Change Template Proposal Approval shows inconsistent behavior

</td></tr><tr><td>

Change Management

</td><td>

PRB1929253

</td><td>

A message from 'Add affected CIs' persists after the list is filtered

</td></tr><tr><td>

Change Management

</td><td>

PRB1929526

</td><td>

Scheduling Assistant shows incorrect time slots on Mondays in 'JST' time zone

</td></tr><tr><td>

Change Management - Risk Assessment and Intelligence

</td><td>

PRB1930532

</td><td>

Change Risk Assessment overrides an Assessments UI Action which has left the UI Actions out of sync

</td></tr><tr><td>

CI Relations Formatter

</td><td>

PRB1964112

</td><td>

g\_builddate isn't defined

</td></tr><tr><td>

Client Scripts

</td><td>

PRB1976513

</td><td>

showFieldMsg is unexpectedly dismissed for the 'Date' and 'Date/time' fields in workspace

</td></tr><tr><td>

Client Scripts

</td><td>

PRB1954396

</td><td>

g\_form.disableAttachments\(\) doesn't work in the onLoad client script when called in callback of GlideAjax

</td></tr><tr><td>

Client Scripts

</td><td>

PRB1956934

</td><td>

g\_form.getActionName returns 'none' when adding a file in a file attachment field

</td></tr><tr><td>

Client Scripts

</td><td>

PRB1926836

</td><td>

Optional chaining in Service Catalog Client Scripts throw an error upon saving

</td></tr><tr><td>

Cloud Provisioning and Governance

</td><td>

PRB1939563

</td><td>

Base instance business rule 'Empty Name Check' results in unexpected abortion due to few names matching the Account ID

</td></tr><tr><td>

Cloud Provisioning and Governance

</td><td>

PRB1941402

</td><td>

sn\_cmp\_ssh\_credentials is automatically created when a catalog form loads

</td></tr><tr><td>

Cloud Provisioning and Governance

</td><td>

PRB1930444

</td><td>

The are empty execution ID entries in the sn\_cmp\_order\_step\_status table when the corresponding order record in sn\_cmp\_order is deleted

</td></tr><tr><td>

CMDB CI Class Manager

</td><td>

PRB1873821

</td><td>

The 'Attributes' column descriptions do not respect dictionary overrides for CI Class Manager

</td></tr><tr><td>

CMDB Data Manager

</td><td>

PRB1893433

</td><td>

CMDB Data Management Task assigned to user is still creating tasks with Managed By User of the CI even if the Dependent CI Policy has Task Assignment User attribute set to a User

</td></tr><tr><td>

CMDB Data Manager

</td><td>

PRB1919568

</td><td>

Archiving can erroneously report a failure when there are over 100 CIs in a chunk

</td></tr><tr><td>

CMDB Data Manager

</td><td>

PRB1771506

</td><td>

Data Management task is first assigned to the user who approved it and then assigned to empty

</td></tr><tr><td>

CMDB Data Manager

</td><td>

PRB1889646

</td><td>

Base instance business rule 'Reset cmdb task approval flow' on 'cmdb\_data\_management\_task' throws an error in the syslog table

</td></tr><tr><td>

CMDB Data Manager

</td><td>

PRB1935628

</td><td>

Suggested relationship types show double relation of 'Used by \(Child\)'

</td></tr><tr><td>

CMDB Health Dashboard

</td><td>

PRB1921545

</td><td>

Can't preview records in the CMDB Health Dashboard List

</td></tr><tr><td>

CMDB Identification and Reconciliation

</td><td>

PRB1920308

</td><td>

The IRE doesn't update the related tables last\_discovered or discovery\_source columns on the ora\_java\_audit table

</td></tr><tr><td>

CMDB Identification and Reconciliation

</td><td>

PRB1939473

</td><td>

SGO-Dynatrace Process Groups create duplicate relationships for the same Parent and Child CI

</td></tr><tr><td>

CMDB Identification and Reconciliation

</td><td>

PRB1952085

</td><td>

Dependent items are inserted regardless of the parent or main CI insertion failure

</td></tr><tr><td>

CMDB Identification and Reconciliation

</td><td>

PRB1893877

</td><td>

Slow query on Orphan Processor

</td></tr><tr><td>

CMDB Identification and Reconciliation

</td><td>

PRB1902220

</td><td>

De-duplication task is not created for ci-items when there is a lookup-item based multi-match

</td></tr><tr><td>

CMDB Identification and Reconciliation

</td><td>

PRB1919434

</td><td>

Reference Fields are not selectable for Hybrid Identification rules

</td></tr><tr><td>

CMDB Query Builder

</td><td>

PRB1982264

</td><td>

There's an inefficient query on cmdb\_rel\_ci - primary\_hash=-739782498

</td></tr><tr><td>

CMDB Query Builder

</td><td>

PRB1848525

</td><td>

In CMDB Query Builder, saved query cards load slowly on instances with many saved queries

</td></tr><tr><td>

CMDB Query Builder

</td><td>

PRB1910646

</td><td>

A large query from Query Builder may lead to excessive memory utilization on a server

</td></tr><tr><td>

CMDB Query Builder

</td><td>

PRB1949470

</td><td>

Each execution of a saved query recreates SYS\_UI\_LIST records, even if not creating a table

</td></tr><tr><td>

CMDB Query Builder

</td><td>

PRB1964608

</td><td>

There's missing column results on pattern query connects to non-CMDB tables

</td></tr><tr><td>

CMDB Query Builder

</td><td>

PRB1966587

</td><td>

Query Execution fails with QB APIs, but succeeds with UI execution

</td></tr><tr><td>

Code Signing

</td><td>

PRB1921400

</td><td>

Update the signature timestamp on JIT-loading when the signature isn't present in the table, and compare the signature timestamp with the plugin upgrade timestamp before loading

</td></tr><tr><td>

Column Level Encryption

</td><td>

PRB1919998

</td><td>

'Save as Draft' for a catalog item doesn't work in a portal when logged in through an Edge proxy

</td></tr><tr><td>

Column Level Encryption

</td><td>

PRB1940680

</td><td>

Additional comment is duplicated when encryption is applied

</td></tr><tr><td>

Column Level Encryption

</td><td>

PRB1940688

</td><td>

For some language translations, the translations exceed the limit

</td></tr><tr><td>

Column Level Encryption

</td><td>

PRB1877801

</td><td>

Fields that are created on the task level table show a different size in UI16 and Next Experience

</td></tr><tr><td>

Column Level Encryption

</td><td>

PRB1892581

</td><td>

KMFCallerAccessPolicyRecordInterface\#getCLECryptoModulesFromCallerPolicyTable isn't cached, causing a performance bottleneck

</td></tr><tr><td>

Column Level Encryption Enterprise

</td><td>

PRB1914308

</td><td>

A column level encrypted field shows encrypted values

</td></tr><tr><td>

Communities

</td><td>

PRB1952833

</td><td>

Blog posts within Community forums have all been reformatted

</td></tr><tr><td>

Communities

</td><td>

PRB1939875

</td><td>

Editing a post and saving throws an error

</td></tr><tr><td>

Communities

</td><td>

PRB1914439

</td><td>

Base instance \(add\_users\_to\_announcement\_list\) is expected to include users based on forum subscription or membership but it doesn't

</td></tr><tr><td>

Communities

</td><td>

PRB1919963

</td><td>

Community emails go out to users even when they opted out

</td></tr><tr><td>

Communities

</td><td>

PRB1925015

</td><td>

The community\_forum\_list widget returns unexpected results when searching with the '&amp;' character

</td></tr><tr><td>

Communities

</td><td>

PRB1930528

</td><td>

Community users can mention other community users in content with @nameOfTheUser, even if those users are inactive and their sys\_user records are not active

</td></tr><tr><td>

Communities

</td><td>

PRB1932974

</td><td>

Unparseable date accessing Activity tab in Community Profile

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1899557

</td><td>

Dot-walked tags fields in Platform Analytics revert back to the original table

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1955570

</td><td>

In the Service Operations Workspace , there are hardcoded strings in the advanced filter

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1927599

</td><td>

The condition builder on the presentational list displays all the options instead of the one that was searched

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1949745

</td><td>

In a newer version of the Workflow Studio filter in Yokohama, the radio choice filter that used to display a string field isn't available

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1935085

</td><td>

In condition builder, the selected choice doesn't show any inactivated values

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1969379

</td><td>

In Platform Analytics, a data source filter with an operator 'is one of' / 'is not one of' displays the NULL/EMPTY option

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1931089

</td><td>

Condition variables dot-walking doesn't populate results on data visualizations

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1949906

</td><td>

Using GT\_FIELD and LT\_FIELD operators for two dotwalk dynamic attributes throws com.glide.ux.runtime.list.gql.NowListLayoutCompositeQuery errors

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1950699

</td><td>

When a user presses 'Enter' on a value in a filter, it unexpectedly adds a keyword field

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1962000

</td><td>

Comparing a catalog item variable to the created date in a report condition isn't working as expected

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1966342

</td><td>

List\_Label isn't announced by a screen reader

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1851527

</td><td>

In some Related List Entry forms, the filter field's choice list does not include any fields from the target table

</td></tr><tr><td>

Condition Builder in Core UI

</td><td>

PRB1936913

</td><td>

Filter condition "Created on last Month" is not working properly

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1918698

</td><td>

Health inclusion rules \(cmdb\_health\_config\) can't be added for certain tables that belong to CMDB CI Class Models

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1894727

</td><td>

Duplicate approvals are created for the same users for CMDB Data manager tasks while in the 'Requested' state

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1969483

</td><td>

The 'CMDB Group Health' dashboard displays incorrect totals for parent metrics

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1909363

</td><td>

CMDB Data Management policy fails to archive records and returns the error 'Failed to create archive chunk. No CIs will be archived under this task'

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1913161

</td><td>

The scheduled script 'Populate Internet Facing attribute on Hardware' can't set internet\_facing=false

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1952210

</td><td>

CMDB related list for 'svc\_ci\_assoc' is incorrectly labeled 'Configuration Item'

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1925115

</td><td>

CSDM Sync business rules for CMDB do not support non-asset CIs if PI sync is enabled

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1966768

</td><td>

If an input contains a lifecycle stage and a lifecycle stage status, an IRE CI update is aborted by the 'Validate lifecycle combination' business rule

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1909506

</td><td>

Database performance is impacted due to the ASYNC: Script job

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1968891

</td><td>

Application Service &gt; Service Instance changes are missed in UI actions

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1923632

</td><td>

CMDB Health Correctness group score doesn't consider inclusion rules when computing health score

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1914626

</td><td>

Insufficient access that's caused by a 'run as' user specification causes fewer records than expected to be included in the generated task

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1933079

</td><td>

Missing lookup table settings attributes on reopening identification rule

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1934365

</td><td>

Change the health dashboard failure threshold to apply only when it exists

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1953125

</td><td>

A multisource domain path isn't set for update scenarios

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1955150

</td><td>

Configuration Item lifecycle validation can abort changes to CI, but still push changes to linked asset

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1956449

</td><td>

A CMDB data certification task in the 'Data Certification' dashboard displays inconsistent data on the 'Review not completed' tab

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1986775

</td><td>

IRE throws missing dependency errors for dependent CIs when glide.identification\_engine.skip\_sys\_object\_source\_matching property is enabled

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB702100

</td><td>

Labels are the same for multiple CMDB-related tables

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1865417

</td><td>

There is no option to create records in the Data Service Instance table \(cmdb\_ci\_data\_service\_instance\)

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1871274

</td><td>

'CMDB Cascade Retire Dependent CIs' is unable to delete the processed CIs

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1877360

</td><td>

Failure to create a new service instance due to auto-numbering issue with base instance data for CSDM

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1894116

</td><td>

CI Install status is set as 'absent' even after a successful discovery

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1904681

</td><td>

The timeline widget \(both classic History Timeline and Unified Map timeline\) in CMDB Workspace doesn't display CI-related changes

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1907569

</td><td>

For CMDB 360 Query 3, Source 1/Source2 are displaying correctly when the 'Compare to CMDB' checkbox is selected and Source 1/Source2 are empty when 'Compare to CMDB' checkbox isn't selected

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1911028

</td><td>

The QB UI throws a 500 error on selecting columns for a node in QB Query construction

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1915178

</td><td>

CMDB Workspace makes calls for i18n that could be fetched

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1917175

</td><td>

Remove redundant overall metric reference from health dashboard

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1924702

</td><td>

The Policy Execution ID field in the cmdb\_data\_management\_task table shows "Completed" as display value

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1926784

</td><td>

Skip invalid tables from health score calculation of CMDB health group

</td></tr><tr><td>

Console

</td><td>

PRB1914597

</td><td>

Script Tracer window with scroll bars moves/shakes constantly while running

</td></tr><tr><td>

Contextual Search

</td><td>

PRB1925445

</td><td>

Contextual Search logs an error message instead of a debug message for an unsupported feature

</td></tr><tr><td>

Contextual Search

</td><td>

PRB1937841

</td><td>

cxs\_relevant\_doc is created with incorrect relevance to \(source\_doc\) so the m2m\_kb\_task record is not created

</td></tr><tr><td>

Contextual Search

</td><td>

PRB1920670

</td><td>

Knowledge Articles don't display in the Related List after being attached from Contextual Search

</td></tr><tr><td>

Contextual Search

</td><td>

PRB1930220

</td><td>

Contextual Search Results cause an error if there is an emoji in any of the text fields

</td></tr><tr><td>

Continual Improvement Management

</td><td>

PRB1927760

</td><td>

Rename function in CIM's UI Action "View KPI details" to avoid conflict with the same function name in "View Scorecard"

</td></tr><tr><td>

Contract Management

</td><td>

PRB1969392

</td><td>

The yearly cost on a contract isn't calculated from active contract rate cards

</td></tr><tr><td>

Contract Management

</td><td>

PRB1972929

</td><td>

If the date format isn't the default system \(YYYY-MM-DD\), users are unable to save or extend contracts through the Hardware Asset Management workspace

</td></tr><tr><td>

Core Platform

</td><td>

PRB1731307

</td><td>

When the function definition is provided, an improper syntax throws 'Record not found' for the corresponding table

</td></tr><tr><td>

Cost Management

</td><td>

PRB1907331

</td><td>

Expense lines record against the wrong cost plan, expense type, and cost type, which causes a difference between exported reports and tables in SPM

</td></tr><tr><td>

Cost Management

</td><td>

PRB1968641

</td><td>

There's an unexpected calculation from the 'fm\_Populate Month Field' business rule

</td></tr><tr><td>

Currency Administration

</td><td>

PRB1940257

</td><td>

Real-time updates on a form display incorrect values in currency fields, causing data loss

</td></tr><tr><td>

Currency Administration

</td><td>

PRB1896464

</td><td>

Instance can't handle properly newly added custom currency code on fx\_currency

</td></tr><tr><td>

Currency Administration

</td><td>

PRB1935621

</td><td>

Issue with currency type field on proc\_po\_item table

</td></tr><tr><td>

Customer Operations for Customer Service Management

</td><td>

PRB1973190

</td><td>

Slow read ACL causes a performance issue

</td></tr><tr><td>

Customer Service Management

</td><td>

PRB1967302

</td><td>

Inactive CSM knowledge bases were reactivated unexpectedly during the upgrade of an instance to Zurich

</td></tr><tr><td>

Customer Service Management

</td><td>

PRB1926263

</td><td>

Users with the roles 'snc\_internal' and 'sn\_customerservice.customer\_data\_viewer' can see all the records from the ast\_contract table

</td></tr><tr><td>

Customer Service Management

</td><td>

PRB1928341

</td><td>

sn\_customerservice\_manager contains workspace\_admin role and can modify global UI Actions like delete, save, update, global forms

</td></tr><tr><td>

Customer Service Management

</td><td>

PRB1931244

</td><td>

Incorrect information message thrown "\[Problem Number\] has been linked to this problem" when linking a problem to a case via Agent Assist

</td></tr><tr><td>

Customer Service Management Workspace

</td><td>

PRB1958198

</td><td>

In CSM/FSM Configurable Workspace, 'No records to display' text is defined as a heading

</td></tr><tr><td>

Data Archiving

</td><td>

PRB1921624

</td><td>

There's a race condition where one record can be archived twice

</td></tr><tr><td>

Database Indexes

</td><td>

PRB1938499

</td><td>

If an element is in a compound index, modifying the max\_length on a table to &gt; 255 throws a SQLException

</td></tr><tr><td>

Database Indexes

</td><td>

PRB1891295

</td><td>

'Drop Index' functionality wasn't following the complete drop index process

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1930261

</td><td>

DB connection recycling reduces the number of available semaphore permits

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1939323

</td><td>

SQLException thrown when loading the sc\_cat\_item table with language translations on \(order by a field that can have translations\)

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1853004

</td><td>

Oracle 'GroupBy a reference field' in Korean fails and throws a syntax error

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1969080

</td><td>

An incorrect column alias is used in query generation when storage\_alias matches element\_name of another column

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1909923

</td><td>

Propagate OrderBy to SELECT sub clause on GlideAggregate when using setAggregateWindow

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1937141

</td><td>

When the user right clicks on the "State" field in the Change task form's configure label option, it throws "record not found"

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1942424

</td><td>

List filtering a choice field by 'starts with' doesn't work for non-English languages

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1962341

</td><td>

Truncating a temporary table using gs.truncateTable\(\) creates a new temporary table

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1962784

</td><td>

Property glide.db.alter\_large\_table\_threshold can't be set large enough

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1965515

</td><td>

Minimize the impact of connection pool expansion throttling on scheduler jobs

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1970223

</td><td>

The DBSqlParser query modifies the sys\_id ElementDescriptor storage table name, which breaks queries to the parent tables after

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1920242

</td><td>

Searching in Italian on a translated text field does not work

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1920823

</td><td>

Data is lost on updateMultiple with the type 'phone number E164'

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1995281

</td><td>

Instant alter on a large table times out after 3 minutes and enters an infinite DDL retry loop, and is an upgrade blocker

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1968109

</td><td>

When glide.db.aggregate.groupby\_display\_optimize is true, group by reference fields display value is a sys\_id

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1715251

</td><td>

There's a syntax error when adding a dot-walked column with the type 'fx\_currency' to a report

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1958519

</td><td>

Datetime truncates values after 'yyyy-MM-dd' in RaptorDB

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1783331

</td><td>

TableDescriptor.isValid\(\) returns true for wrongly cased logical table names with function field columns

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1939121

</td><td>

WhereClause isn't correctly identified when language translations are enabled for a catalog variable with reference to sc\_cat\_item

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1891512

</td><td>

FixNonAsciiColumnNames jobs should be able to handle unexpected errors and still carry out cache flush

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1969095

</td><td>

Old value is being encrypted

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1928920

</td><td>

ScheduleDateTime extending String \(and mapped to VARCHAR\) causes string comparison instead of DateTime comparison in SQL queries

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1942103

</td><td>

getForTables gives inactive columns

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1943465

</td><td>

'Is Not' with multiple 'OR' Conditions results in incorrect results

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1971470

</td><td>

Column visualization shows incorrect data if the week start is different from Sunday or Monday

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1978837

</td><td>

Glide online ALTER DDL statements can be stuck in 'wait for metadata lock', which can cause database lock and semaphore exhaustion

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1792470

</td><td>

Some alters to increase max length are running twice during an upgrade

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1825857

</td><td>

Unused and missing joins in query generation for a TS query with many 'contains' conditions

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1871451

</td><td>

Query business rules aren't honored in GraphQueryExecutors

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1889308

</td><td>

On RaptorDB, a Function field definition using divide with a fractional dividing value ignores the fractional component and only uses the non-fractional value

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1903695

</td><td>

The 'between' operator on a function field from a reference column returns incorrect query/data

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1905616

</td><td>

Issue with filtering a Translated text field when it is empty in the French language

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1923704

</td><td>

Due to an ordering change on Raptor post migration, certificate authentications for API calls may fail and cause '500' errors

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1929018

</td><td>

C2R isn't working when query has '\\'

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1930341

</td><td>

Choice field max length is ignored in the storage column selection, which may lead to the value truncation

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1930611

</td><td>

GlideRecord.find\(\) can create a duplicate record

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB1884666

</td><td>

TableCleaner. deleteAttachments\(\) has an infinite loop and is unable to delete encrypted records

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB1971093

</td><td>

One-time update/delete job conditions shouldn't contain Javascript

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB1939498

</td><td>

Migration to RaptorDB brings column length changes, which could impede archive table synchronization

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB1982941

</td><td>

Collection records in sys\_dictionary are unexpectedly cascade deleted

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB1894495

</td><td>

The 'Glide clone' API isn't generating delete statements for a hybrid table

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1860988

</td><td>

An instance became inaccessible after testing

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1975852

</td><td>

MetricStatsCache causes the application node to run OutOfMemory

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1889276

</td><td>

deleteMultiple fails for PG for IN conditions larger than 1000

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1908288

</td><td>

Canceled transactions don't finish until the query has completed when loading a result set

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1878883

</td><td>

Update the Table Cleaner rule to target more dead records

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1945816

</td><td>

A connection pool should properly handle errors during expansion

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1893786

</td><td>

Truncate oversized CLOBs to 16M because the job causes long running transactions in RaptorDB and blocks multiple sessions

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1928060

</td><td>

Deactivating the secondary pool record in sys\_db\_pool does not shut down the actual DB Connection Pool.

</td></tr><tr><td>

Database Rotation

</td><td>

PRB1954418

</td><td>

A sys\_created\_on filter doesn't work for a shard-type rotation

</td></tr><tr><td>

Database Views

</td><td>

PRB1881428

</td><td>

A MariaDB database view using INSTR could result in a syntax error when the function is rewritten when executed because of a related &gt; 0 or != 0 comparison

</td></tr><tr><td>

Data Policies

</td><td>

PRB1840624

</td><td>

Setting a read-only data policy on an HTML type field causes an invalid error to occurr after downloading the attachment

</td></tr><tr><td>

Data Privacy \(Classic\)

</td><td>

PRB1940538

</td><td>

Clone job depends on the 'dp\_rta\_ner\_request' table to run successfully

</td></tr><tr><td>

Data Privacy \(Classic\)

</td><td>

PRB1943631

</td><td>

An overriding record shouldn't be in the global domain

</td></tr><tr><td>

Data Privacy \(Classic\)

</td><td>

PRB1960061

</td><td>

Keywords in data pattern causes false positive discovery

</td></tr><tr><td>

Data Privacy \(Classic\)

</td><td>

PRB1919038

</td><td>

dp\_cache\_refresh\_thread\_name thread deadlock scenarios

</td></tr><tr><td>

Data Snapshots

</td><td>

PRB1958979

</td><td>

**Apply target color to icon** doesn't work for a DS indicator

</td></tr><tr><td>

Data Snapshots

</td><td>

PRB1953187

</td><td>

DataSnapshot is not supported and causes errors in the System Log / Error Log

</td></tr><tr><td>

Date Picker

</td><td>

PRB1896055

</td><td>

Field of the type 'Basic Date/Time' behaves not as expected on the UI when the date format does not match the base instance 'yyyy-MM-dd glide.sys.date\_format

</td></tr><tr><td>

Declarative Actions

</td><td>

PRB1819856

</td><td>

Declarative actions \(Move, Add, Change, Delete\) aren't enabled when 'group by' is applied on any column for active PI records

</td></tr><tr><td>

Declarative Actions

</td><td>

PRB1972195

</td><td>

Declarative actions disappear after navigating to an invalid record in the workspace due to a 'Form Action Layout' caching issue.

</td></tr><tr><td>

Declarative Actions

</td><td>

PRB1955274

</td><td>

ReferenceDecoratorUtils. showRefDecorator\(\) doesn't return the correct value

</td></tr><tr><td>

Declarative Actions

</td><td>

PRB1839630

</td><td>

The re-size modal from the list view isn't not working in workspace

</td></tr><tr><td>

Declarative Actions

</td><td>

PRB1930569

</td><td>

Reference qualifier query for UX action in Action Form Layout Group is partially incorrect

</td></tr><tr><td>

Dependency Views

</td><td>

PRB1960563

</td><td>

The 'ngbsm\_view', which isn't domain separated, can display users and CIs references from different domains

</td></tr><tr><td>

Developer Sandboxes

</td><td>

PRB1952287

</td><td>

If a plugin is turned off, xmlstats?include=dsb\_stats shouldn't return any DSB information

</td></tr><tr><td>

Discovery

</td><td>

PRB1969791

</td><td>

The Discovery Pattern logs say Warning CI Pattern is completed, even though the pattern failed completely

</td></tr><tr><td>

Discovery

</td><td>

PRB1905069

</td><td>

Discovery can fire both discovery.completed and discovery.canceled events, which results in any 'run after' schedules being triggered twice

</td></tr><tr><td>

Discovery

</td><td>

PRB1946099

</td><td>

AWS Cloud schedules are not working as expected

</td></tr><tr><td>

Discovery

</td><td>

PRB1951250

</td><td>

Use bash shell when the command contains a semi-colon

</td></tr><tr><td>

Discovery

</td><td>

PRB1857955

</td><td>

Discovery Jobs on Mutual Auth MID Servers have a big increase in duration

</td></tr><tr><td>

Discovery

</td><td>

PRB1915033

</td><td>

Unable to download private key after generating CSR in certificate management request

</td></tr><tr><td>

Discovery

</td><td>

PRB1956011

</td><td>

ADM / ADME probes cause memory issues and take down instance nodes due to large amount of PostgreSQL processes discovered

</td></tr><tr><td>

Discovery

</td><td>

PRB1916388

</td><td>

Discovery admin user is unable to view the error records for a Discovery schedule

</td></tr><tr><td>

Discovery

</td><td>

PRB1964984

</td><td>

'Pattern Sync to Mid' UI action causes OOM on instances with large number of custom fields

</td></tr><tr><td>

Discovery

</td><td>

PRB1893089

</td><td>

The 'Discovery::getScheduleContainingAnyIP\(\)' API causes slow pressing of 'change\_request.trigger.discovery' sysevents

</td></tr><tr><td>

Discovery

</td><td>

PRB1907392

</td><td>

Dell EMC Data Domain pattern fails to discover the device

</td></tr><tr><td>

Discovery

</td><td>

PRB1924351

</td><td>

NoSuchElementException in SNMP \(v2c\) Response Processing

</td></tr><tr><td>

Discovery

</td><td>

PRB1898199

</td><td>

DiscoveryAPI doesn't work in Flow

</td></tr><tr><td>

Discovery

</td><td>

PRB1950443

</td><td>

Look into adding timeout values for Credentialless NMAP discovery to potentially avoid hung threads/memory issues

</td></tr><tr><td>

Discovery

</td><td>

PRB1926888

</td><td>

File Based Discovery omits the capture of the 'Last Scanned' field

</td></tr><tr><td>

Discovery

</td><td>

PRB1773487

</td><td>

'Quick Discovery' is slow because of global IP exclusion processing

</td></tr><tr><td>

Discovery

</td><td>

PRB1853651

</td><td>

An auto-retry mechanism is needed when discovery jobs input probe processing fails to insert the sys\_trigger record

</td></tr><tr><td>

Discovery

</td><td>

PRB1935662

</td><td>

Devices are misclassified as Router/Switch instead of Firewall

</td></tr><tr><td>

Discovery

</td><td>

PRB1936605

</td><td>

Multiple 'Panorama Security policies' patterns fail because the name of the group has spaces

</td></tr><tr><td>

Discovery

</td><td>

PRB1383768

</td><td>

There should be an option for MID clusters in Serverless Discovery schedules

</td></tr><tr><td>

Discovery

</td><td>

PRB1885328

</td><td>

TLS Handshake Scanner currently doesn't support TLSv1.3; the implementation is hardcoded to use TLSv1.2 only

</td></tr><tr><td>

Discovery

</td><td>

PRB1896042

</td><td>

Discovery Pattern fails to explore on Linux servers

</td></tr><tr><td>

Discovery

</td><td>

PRB1970237

</td><td>

Post-Zurich upgrade, pattern debug mode isn't working as expected

</td></tr><tr><td>

Discovery

</td><td>

PRB1893063

</td><td>

For SNMP Shazzam, if there's Cred Affinity to V3 credential, V3 should be tried first, and V1/V2 should only be tried after

</td></tr><tr><td>

Discovery

</td><td>

PRB1925320

</td><td>

Payload processing steps are incorrectly placed in horizontal logs

</td></tr><tr><td>

Discovery

</td><td>

PRB1909689

</td><td>

A pattern step fails intermittently due to the 'runCommand' being null

</td></tr><tr><td>

Discovery

</td><td>

PRB1956992

</td><td>

Discovery logs display an error when ci\_sys\_id doesn't exist or the value of OS field/column is NULL: 'TypeError: Cannot convert null to an object'

</td></tr><tr><td>

Discovery

</td><td>

PRB1959120

</td><td>

The 'VMWarevCenterESXHostsProbe' probe doesn't update the 'Last Scanned' field for vSphere software installations

</td></tr><tr><td>

Discovery

</td><td>

PRB1913970

</td><td>

Using VM &gt; config &gt; guestFullName causes a discrepancy in guest\_os\_fullname in Discovery

</td></tr><tr><td>

Discovery

</td><td>

PRB1975276

</td><td>

Typo in encoded query

</td></tr><tr><td>

Discovery

</td><td>

PRB1903928

</td><td>

Slow query with primary\_hash=-865319141 runs 60k times per day, consuming reasonable time from the database

</td></tr><tr><td>

Discovery

</td><td>

PRB1938420

</td><td>

HTTP pattern fails with the error "MULTIPLE\_DEPENDENCIES Found multiple dependent relation items"

</td></tr><tr><td>

Discovery

</td><td>

PRB1939261

</td><td>

User with discovery\_admin role unable to see "Test Probe" UI action under Related links

</td></tr><tr><td>

Discovery

</td><td>

PRB1939533

</td><td>

The mac\_manufacturer field on cmdb\_ci\_network\_adapter is not populated by base instance discovery

</td></tr><tr><td>

Discovery

</td><td>

PRB1939856

</td><td>

Some servers get retired during discovery after updating Visibility Content to version 6.26.0

</td></tr><tr><td>

Discovery

</td><td>

PRB1944007

</td><td>

The SNMP OID classification model is incorrect for the OID '1.3.6.1.4.1.1872.1.13.3.5" / "1.3.6.1.4.1.1872.1.13.3.5.2'

</td></tr><tr><td>

Discovery

</td><td>

PRB1946539

</td><td>

The SNMP OID 1.3.6.1.4.1.5003.8.1.1.56 number belongs to Voice Gateway, but its incorrectly updated as 'router'

</td></tr><tr><td>

Discovery

</td><td>

PRB1947421

</td><td>

Discovery's 'Connecting to' and 'Listening on' fields display ':undefined:' instead of 'port'

</td></tr><tr><td>

Discovery

</td><td>

PRB1960086

</td><td>

'Discovery credential' list view still displays a MID Server after switching to 'Applies to All MID Servers'

</td></tr><tr><td>

Discovery

</td><td>

PRB1962473

</td><td>

The 'AWS Org Assume Role' fails when using wildcard ARN containing an IAM role path

</td></tr><tr><td>

Discovery

</td><td>

PRB1966593

</td><td>

ECC queues with empty agent\_correlator cause errors on a Discovery job

</td></tr><tr><td>

Discovery

</td><td>

PRB1968412

</td><td>

DiscoverySensorJob script includes have gs.info statements that fill the syslog table and can't be turned off

</td></tr><tr><td>

Discovery

</td><td>

PRB1969220

</td><td>

"AbstractDeleteStrategy" generates queries from "sys\_object\_source" with an excessively large number of "target\_sys\_id"

</td></tr><tr><td>

Discovery

</td><td>

PRB1972668

</td><td>

SSM starved all MID threads

</td></tr><tr><td>

Discovery

</td><td>

PRB1979768

</td><td>

After a Zurich upgrade, in ACC, there's a discovery source issue for some server records set from ACC-Visibility to ServiceNow

</td></tr><tr><td>

Discovery

</td><td>

PRB1785169

</td><td>

ACC-V execution for Oracle GLAS Data Collection fails because the pattern removes 'ct\_cpuq.sh' and 'db\_queries\_to\_csv.sql' as part of the 'Target Cleanup' process

</td></tr><tr><td>

Discovery

</td><td>

PRB1835558

</td><td>

The 'Put file' operation does not filter credentials based on credential tag

</td></tr><tr><td>

Discovery

</td><td>

PRB1875973

</td><td>

Multipage doesn't break pages properly when there's a large number of related items on the main CI, and 1000+ pages are created; however most pages have only a few objects

</td></tr><tr><td>

Discovery

</td><td>

PRB1878387

</td><td>

Domain picker option exploration for filtering data as per domain for Discovery Admin Workspace

</td></tr><tr><td>

Discovery

</td><td>

PRB1891908

</td><td>

Warning message for Cloud Discovery will display for non-Cloud Discovery schedules

</td></tr><tr><td>

Discovery

</td><td>

PRB1892035

</td><td>

ITOM Content Service true up for Zurich

</td></tr><tr><td>

Discovery

</td><td>

PRB1895238

</td><td>

Cloud Application Patterns are launched sequentially and contribute to the long discovery schedule

</td></tr><tr><td>

Discovery

</td><td>

PRB1895406

</td><td>

Cleanup of stale relationships in VMware Discovery \(vMotion and vCenter Migration\)

</td></tr><tr><td>

Discovery

</td><td>

PRB1895555

</td><td>

Cannot recover stale Cloud Discovery schedules due to sensor transaction timeout

</td></tr><tr><td>

Discovery

</td><td>

PRB1895680

</td><td>

Discovery being executed against retired NICs

</td></tr><tr><td>

Discovery

</td><td>

PRB1898371

</td><td>

Cisco Next Generation Firewall pattern is using SNMP for hostname despite glide.discovery.hostname.snmp\_trusted being 'false'

</td></tr><tr><td>

Discovery

</td><td>

PRB1902724

</td><td>

Disable the debug message in Discover Logs for credential-less IP address in payload because it is null and creating PRBs

</td></tr><tr><td>

Discovery

</td><td>

PRB1907740

</td><td>

Inefficient deletion strategy during snapshot cleanup is causes performance issues and affects Discovery runs

</td></tr><tr><td>

Discovery

</td><td>

PRB1911156

</td><td>

EMC Isilon discovery relevant basic authentication credentials are used

</td></tr><tr><td>

Discovery

</td><td>

PRB1911645

</td><td>

Fortinet firewalls are incorrectly classified as routers on instances that were initially provisioned before Vancouver and updated to Vancouver or later

</td></tr><tr><td>

Discovery

</td><td>

PRB1912063

</td><td>

Version upgrade creates duplicate SNMP public credential

</td></tr><tr><td>

Discovery

</td><td>

PRB1913340

</td><td>

SuSE Linux OS is not retrieving the clusters

</td></tr><tr><td>

Discovery

</td><td>

PRB1915654

</td><td>

Behaviors don't work for IPv6 addresses or host names on a schedule

</td></tr><tr><td>

Discovery

</td><td>

PRB1916283

</td><td>

Credential Affinity is not used for CIM - Classify when an external credential is used

</td></tr><tr><td>

Discovery

</td><td>

PRB1917904

</td><td>

File Details probe causes ECC output records to be generated with mid.server.undefined

</td></tr><tr><td>

Discovery

</td><td>

PRB1918198

</td><td>

Unexpected Type values in Database class set by discovery

</td></tr><tr><td>

Discovery

</td><td>

PRB1922628

</td><td>

Resolve High CPU utilization due to ServiceNow discovery commands running on AIX servers

</td></tr><tr><td>

Discovery

</td><td>

PRB1925371

</td><td>

The operational status for remove AWS resources is not updated to 'Retired' after discovery execution

</td></tr><tr><td>

Discovery

</td><td>

PRB1931349

</td><td>

Script evaluation error in script include "VCenterVmStateUpdater" causes errors in the syslog

</td></tr><tr><td>

Discovery for Amazon Web Service \(AWS\) cloud

</td><td>

PRB1922763

</td><td>

Amazon "Secret Region" C2S, has a non "amazonaws.com" sts endpoint, which is currently unsupported

</td></tr><tr><td>

Discovery Probes and Sensors

</td><td>

PRB1901850

</td><td>

Discovery Probe warnings 'HOSTARRAY\[index++\]=server \{: not found'

</td></tr><tr><td>

Discovery Probes and Sensors

</td><td>

PRB1948780

</td><td>

The script include 'ClassifierProbes' isn't using SelfCleaningMutex

</td></tr><tr><td>

Discovery Probes and Sensors

</td><td>

PRB1959013

</td><td>

Linux distribution's 'Rocky' gets classified as a generic 'GNU/Linux' operating system

</td></tr><tr><td>

Document Intelligence Unified Backend

</td><td>

PRB1942585

</td><td>

Straight-through processed documents with tables will generate an extra row of predictions if the use case is on a version older than 27.1

</td></tr><tr><td>

Document Management

</td><td>

PRB1934576

</td><td>

HRC document generation does not format correctly

</td></tr><tr><td>

Document Management

</td><td>

PRB1944622

</td><td>

Japanese file names are truncated when downloaded from a shared link

</td></tr><tr><td>

Document Management

</td><td>

PRB1965416

</td><td>

When setting a sequence of approvers for documents, the flow action that processes those approvals evaluates the sequence incorrectly, resulting in disorder

</td></tr><tr><td>

Document Management

</td><td>

PRB1914034

</td><td>

Base instance notification settings are not configured to send document approval rejection notifications to the document owner in Document Management

</td></tr><tr><td>

Document Viewer

</td><td>

PRB1945206

</td><td>

Starting in the Yokohama release, duplicate PDF headers are generated when exporting to PDF file from record form

</td></tr><tr><td>

Document Viewer

</td><td>

PRB1707280

</td><td>

A small lag while loading the document in an iFrame while using the Document Viewer in Now Mobile

</td></tr><tr><td>

Domain Separation

</td><td>

PRB1957915

</td><td>

The error 'com.glide.domain.paths: Domain node missing path with id' causes stack overflow in restart

</td></tr><tr><td>

Domain Separation

</td><td>

PRB1935652

</td><td>

The "Domain - Cascade Company" business rule does not check for a NULL value for the COMPANY filter, resulting in data corruption

</td></tr><tr><td>

Domain Separation

</td><td>

PRB1909848

</td><td>

Updating group membership can delete non-visible members for Domain Separation

</td></tr><tr><td>

Domain Separation

</td><td>

PRB1921443

</td><td>

A default domain exists as both demo data and vase instance data

</td></tr><tr><td>

Dynamic Scheduling

</td><td>

PRB1925058

</td><td>

Dynamic scheduling issues from case tasks

</td></tr><tr><td>

Dynamic Scheduling

</td><td>

PRB1951019

</td><td>

Dynamic scheduling doesn't assign tasks to agents

</td></tr><tr><td>

Dynamic Scheduling

</td><td>

PRB1951608

</td><td>

In Dynamic Scheduling, auto-assignment of some work order tasks take time before a recommendation is displayed

</td></tr><tr><td>

Dynamic Translation

</td><td>

PRB1910384

</td><td>

Translate button isn't visible in the Standard Ticket Conversations widget when the size is less than 768px or it's seen in mobile view

</td></tr><tr><td>

Dynamic Translation

</td><td>

PRB1913176

</td><td>

A One API Service Plan feature for Virtual Agent's \(VA\) Utterance Translation has no timeout set

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

Dynamic Translation for Virtual Agent

</td><td>

PRB1927624

</td><td>

Dynamic translation with live agent conversation in page

</td></tr><tr><td>

Edge Encryption

</td><td>

PRB1927436

</td><td>

After an upgrade to Yokohama, a lot of 'MultiPartXXX' files are created under the 'tmp' folder

</td></tr><tr><td>

Edge Encryption

</td><td>

PRB1915259

</td><td>

Users are uable to attach a 10MB file to a record when logged in with an Edge URL

</td></tr><tr><td>

Edit List Columns

</td><td>

PRB1819221

</td><td>

Choice filter options are not selected by default

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1857979

</td><td>

The 'Email recipients' field in the email client isn't updated in sys\_email\_draft when applying another email client template

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1939486

</td><td>

Base instance email layout &lt;img&gt; missing alt text

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1953887

</td><td>

On the 'Compose email' page, selecting an icon that opens a side panel incorrectly displays the Email Template panel first

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1939810

</td><td>

The NOTIF\_UNSUB macro is translated in static email notifications when the user's notification language isn't English

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1954629

</td><td>

Glide.email.outbound.mailscript\_insecure\_substitution property should be honored for email client

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1914312

</td><td>

User receives SMS alerts for unsubscribed notifications

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1938128

</td><td>

Notification preview should handle scenarios where sysparm\_record\_id is null

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1941865

</td><td>

Multiple deletion isn't throwing any alerts

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1942294

</td><td>

UI16 email client accepts an incorrect format of input for To/Cc/Bcc fields

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1956095

</td><td>

sys\_email records display emails sent from native workbench as 'send-ignored', but the same email sent from Service Operations Workspace displays 'sent'

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1959769

</td><td>

Email templates, response templates, and quick messages aren't displayed in the side panel even though they are present

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1971098

</td><td>

Chevron icons for 'Reply/Reply All/Forward' aren't visible for long email subjects in CSM/FSM Configurable Workspace

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1857521

</td><td>

Addresses are removed from recipients with no explanation or logging

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1900285

</td><td>

Delegated user gets notification emails for non-subscribed notifications

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1904205

</td><td>

The 'Preview Email' notification uses an existing event, and deletes the body of the preview email body

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1906050

</td><td>

Duplicate emails are sent when a recipient is part of Group/Recipient-list for MIM

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1920101

</td><td>

"Check From field" Business Rules display an Error message when there is no error

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1922141

</td><td>

Notification Email Address Filter not working consistently

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1923167

</td><td>

getDisplayValue is does not identify the non-global choices

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1924395

</td><td>

Dynamic email translation fails when the corresponding 'sn\_dt\_translator\_configuration' record is in a non-global domain

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1927781

</td><td>

Existing flows with inbound email trigger do not display advanced options after setting glide.hub.flow.inbound\_email\_trigger.show\_advanced to true

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1928166

</td><td>

Email Client Template 'Reply all' populates the recipient email that received it

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1931000

</td><td>

Emails listed on table sys\_blocked\_email\_address are still receiving emails

</td></tr><tr><td>

Employee Document Management

</td><td>

PRB1894984

</td><td>

Unable to search document types in a non-English language in Employee Document Management

</td></tr><tr><td>

Employee Document Management

</td><td>

PRB1915008

</td><td>

StreamPipeline probe doesn't escape parentheses \(\) in file names in the SCP command line, causing syntax errors

</td></tr><tr><td>

Employee Relations Case Management

</td><td>

PRB1939005

</td><td>

HRSD Email recommendation skill is not working

</td></tr><tr><td>

Employee Relations Case Management

</td><td>

PRB1909215

</td><td>

There's no base instance scoped ACL for sn\_hr\_er and asmt\_assessment\_instance\_question

</td></tr><tr><td>

Employee Service Center

</td><td>

PRB1970121

</td><td>

Description for a catalog item in Now Mobile is not fully in portrait mode even when swiping right; only when switched to landscape mode, the entire content comes

</td></tr><tr><td>

Employee Taxonomy Framework

</td><td>

PRB1897473

</td><td>

A user is able to see expired articles if they are featured

</td></tr><tr><td>

Employee Taxonomy Framework

</td><td>

PRB1875126

</td><td>

Strings are not getting translated

</td></tr><tr><td>

Employee Taxonomy Framework

</td><td>

PRB1936297

</td><td>

The 'Topic path' field on Topic record in Employee center Taxonomy is not properly captured in Update sets

</td></tr><tr><td>

Employee Taxonomy Framework

</td><td>

PRB1899194

</td><td>

Connected Content sort order is not retained for new KB article versions

</td></tr><tr><td>

Encryption Support

</td><td>

PRB1973482

</td><td>

Search filter 'startsWith' is not working on a referenced column when another column with the same name has an EFC

</td></tr><tr><td>

Encryption Support

</td><td>

PRB1911828

</td><td>

The 'Add Attachments' upload stays in an indefinite loading state when selecting 'Close modal' on the Encrypt Attachment

</td></tr><tr><td>

Enterprise Architecture

</td><td>

PRB1945436

</td><td>

When creating a business application, the model\_id is set to 'Unknown'

</td></tr><tr><td>

Enterprise Architecture

</td><td>

PRB1958577

</td><td>

The 'Restrict past target date' business rule aborts an update when planned\_disposition\_date is the current date

</td></tr><tr><td>

Enterprise Architecture integration with Policy and Compliance

</td><td>

PRB1906743

</td><td>

Slow ACL for sys\_security\_acl\_f746285e532101100f61ddeeff7b1285

</td></tr><tr><td>

Event Management

</td><td>

PRB1937156

</td><td>

Events are duplicated multiple times for the same resource of NNMI

</td></tr><tr><td>

Event Management

</td><td>

PRB1941171

</td><td>

Slow query in Event Management - Process Events

</td></tr><tr><td>

Event Management

</td><td>

PRB1975115

</td><td>

Slow processing of the 'Event Management - Maintenance Calculator' job when processing a large number of closed alerts

</td></tr><tr><td>

Event Management

</td><td>

PRB1885972

</td><td>

The 'Solarwinds Volume events' event rule, which was previously deactivated in Washington, is active again after an upgrade to Yokohama

</td></tr><tr><td>

Event Management

</td><td>

PRB1902287

</td><td>

Can't uninstall sn\_em\_ai\_overview and sn\_em\_ai\_action because they're part of core-ui-components/'Core UI Components'/sn\_core\_ui\_ponents

</td></tr><tr><td>

Event Management

</td><td>

PRB1954172

</td><td>

Automated group is created even if some of the alerts don't match the aggregated alerts filter

</td></tr><tr><td>

Event Management

</td><td>

PRB1591528

</td><td>

NNMi connector timestamp is null on em\_event records

</td></tr><tr><td>

Event Management

</td><td>

PRB1934096

</td><td>

There's a regex preview mismatch in Enrich due to Java vs JavaScript engine differences

</td></tr><tr><td>

Event Management

</td><td>

PRB1934829

</td><td>

getMap runs indefinitely when it has an alert path on a service map with a cycle

</td></tr><tr><td>

Event Management

</td><td>

PRB1938724

</td><td>

When setting an alert management rule on a CI name which contains the word "services" the user observes the warning message: "The Impacted Services field in the alert filter is not supported"

</td></tr><tr><td>

Event Management

</td><td>

PRB1942702

</td><td>

Alerts without priority are displayed at the top of a list even though they might be low priority or filtered out

</td></tr><tr><td>

Event Management

</td><td>

PRB1955822

</td><td>

Out of memory errors when processing EM events with additional info &gt; 4000 where event rule CI binding is of type 'CI Field matching for Oracle DB Instances'

</td></tr><tr><td>

Event Management

</td><td>

PRB1956638

</td><td>

Too many EM bi-directional syncs cause the MID Server status to flip

</td></tr><tr><td>

Event Management

</td><td>

PRB1639714

</td><td>

Alerts on an Application Service have empty PRCs

</td></tr><tr><td>

Event Management

</td><td>

PRB1891360

</td><td>

Launch Application contains broken links

</td></tr><tr><td>

Event Management

</td><td>

PRB1891871

</td><td>

em\_events with the resolution state 'Closing' aren't processed correctly during the CEST clock change window

</td></tr><tr><td>

Event Management

</td><td>

PRB1892217

</td><td>

Add logs for the 'Event Management - Update Health Monitor' job

</td></tr><tr><td>

Event Management

</td><td>

PRB1894242

</td><td>

SCOM Connector Bi-Directional update does not update the SCOM Source when the user's language is not English

</td></tr><tr><td>

Event Management

</td><td>

PRB1895330

</td><td>

ImpactStatus isEquals tries to compare non-existent ImpactStatusKey

</td></tr><tr><td>

Event Management

</td><td>

PRB1898882

</td><td>

SCOM Connector update queues are failing

</td></tr><tr><td>

Event Management

</td><td>

PRB1906529

</td><td>

The TBAC 'Override group description' doesn't work on Zurich

</td></tr><tr><td>

Event Management

</td><td>

PRB1911465

</td><td>

Table cleaner of em\_alert does not clean audit records

</td></tr><tr><td>

Event Management

</td><td>

PRB1916071

</td><td>

em\_impact\_maint\_ci 'CI Window Status' field does not update

</td></tr><tr><td>

Event Management

</td><td>

PRB1916917

</td><td>

Negative values in impact status contribution vector

</td></tr><tr><td>

Event Management

</td><td>

PRB1918087

</td><td>

Poor performance of building business service trees in 'Services Dashboard'

</td></tr><tr><td>

Event Management

</td><td>

PRB1929647

</td><td>

OOM error due to 'ASYNC: Event rule grouping calculation' job

</td></tr><tr><td>

Event Management

</td><td>

PRB1930911

</td><td>

Exception when running 'Service Analytics Alert Aggregation Learner - Daily' job when queried alerts in sa\_analytic\_alert has the same remote time

</td></tr><tr><td>

External User Self-Registration

</td><td>

PRB1967636

</td><td>

In external user self-registration, Google captcha loads inconsistently

</td></tr><tr><td>

Field Service Contractor Portal

</td><td>

PRB1978290

</td><td>

Attachments on questionnaires aren't working using the Field Service Management Contractor Portal

</td></tr><tr><td>

Field Service Management

</td><td>

PRB1971866

</td><td>

After an agent selects the 'Reject' UI action, the work order task \(WOT\) redirects to the 'Task reject' UI page

</td></tr><tr><td>

Field Service Scheduling

</td><td>

PRB1949408

</td><td>

There's incorrect Google travel durations when the number of locations exceed matrix\_size

</td></tr><tr><td>

Field Service Scheduling

</td><td>

PRB1930252

</td><td>

"Could not serialize value" occurs in subflows

</td></tr><tr><td>

Field Service Task Bundling

</td><td>

PRB1952595

</td><td>

Scheduling subtasks takes longer than expected

</td></tr><tr><td>

File-based Discovery

</td><td>

PRB1922861

</td><td>

A change in the file information record can be mapped to a new file set, but the software install is not recreated

</td></tr><tr><td>

File-based Discovery

</td><td>

PRB1936524

</td><td>

File-based Discovery doesn't capture the content when the filename contains spaces

</td></tr><tr><td>

Filter Conditions

</td><td>

PRB1941809

</td><td>

Users can't overwrite a Japanese filter \(sys\_filter\)

</td></tr><tr><td>

Filter Conditions

</td><td>

PRB1927694

</td><td>

Show matching break query with the ^NQ

</td></tr><tr><td>

Finance Service Management \(Legacy\)

</td><td>

PRB1957612

</td><td>

A task record was auto-created unexpectedly from a time worked entry

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1925181

</td><td>

The Script API inForeground run a subflow that calls another subflow that has mid action step throws an exception before the outputs are ready with a message

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1903013

</td><td>

A flow execution step that calls a Now Assist skill kit is failing because it's sending back 'null' as the response from the skill kit

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1850198

</td><td>

Output of PowerShell action step is escaping double quotes

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1936210

</td><td>

High priority events aren't cached to the same node due to yield check

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1967018

</td><td>

Instance outage and default semaphore exhaustion is caused by a long-running database query from the GlideElementWorkflow.queryStageState\(\) function

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1971237

</td><td>

Unable to run 65M Load Test

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1907242

</td><td>

Published flow switched from CRUD trigger to email trigger doesn't create sys\_flow\_email\_trigger

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1935825

</td><td>

Skip\_schedule\_cleanup is not reset to false for subflows

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1982762

</td><td>

Unable to queue interactive job IDs for flow.fire events, even though the jobs are queued and the event has been processed

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1912954

</td><td>

Dates do not function to determine uniqueness for 'Insert' or 'Update Record' operations

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1913968

</td><td>

High query count on sys\_flow\_record\_trigger

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1921338

</td><td>

Flows execute repeatedly despite the 'Run Trigger Type' field being set to 'Once'

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1930687

</td><td>

Non-null Runtime values become null after de-serialization on MID

</td></tr><tr><td>

Flow Generation \(Family\)

</td><td>

PRB1915407

</td><td>

The Now Assist flow builder bypasses system rules

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1868564

</td><td>

The Now Mobile App shows more stages on Requested Item records than what's shown in the platform list view for the same record

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1956539

</td><td>

Changing a subflow input name case breaks a flow save

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1945637

</td><td>

Existing scripted fields are set to the 'fd-scripted' static value when there are more than 1 scripted inputs present in the case of templated fields on an update

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1952110

</td><td>

Cross-scope privileges aren't honored in a look-up record action

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1954202

</td><td>

Nested complex objects don't preserve dropped pills

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1878615

</td><td>

Number of decision rows are affecting flow publishing

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1888427

</td><td>

Flow generated from Now Assist does not have an 'AI generated' version

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1904699

</td><td>

There's a null pointer exception on a parent flow if child flow outputs are changed for QUICK flows

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1918469

</td><td>

There's error checking availabilty for a flow recommendations skill

</td></tr><tr><td>

Form Controller

</td><td>

PRB1958159

</td><td>

In CSM/FSM Configurable Workspace, the heading structure is incorrect for the 'Record Information' section

</td></tr><tr><td>

Form Controller

</td><td>

PRB1990803

</td><td>

Users are unable to toggle checkboxes on system properties UI pages

</td></tr><tr><td>

Form Controller

</td><td>

PRB1913291

</td><td>

TAGs created from Service Operations Workspace \(SOW\) doesn't update the 'Title' with name or number in Label entries

</td></tr><tr><td>

Form Controller

</td><td>

PRB1920605

</td><td>

On Workspace, when Special Handling Notes have a condition on a custom field, the Notes are popping up on New Records

</td></tr><tr><td>

Form Templates

</td><td>

PRB1959535

</td><td>

A Knowledge Article body isn't applied when using templates after upgrading Zurich

</td></tr><tr><td>

Form Templates

</td><td>

PRB1919984

</td><td>

Form templates fail to load in workspace if a template with an empty name exists

</td></tr><tr><td>

Form Templates

</td><td>

PRB1963747

</td><td>

A template sometimes can't populate both the 'Assigned to' and 'Assignment' group

</td></tr><tr><td>

Form Templates

</td><td>

PRB1923266

</td><td>

Can't apply form templates in Workspace if a template sets a field which no longer exists on a table

</td></tr><tr><td>

Form Templates

</td><td>

PRB1962327

</td><td>

Users with only the template\_editor role can unexpectedly delete a group template they didn't create

</td></tr><tr><td>

Form Templates

</td><td>

PRB1897466

</td><td>

Searching the templates with short description shows no results

</td></tr><tr><td>

Form Templates

</td><td>

PRB1906244

</td><td>

Form Templates are not applying the value to translated HTML fields when the language is not English for Yokohama

</td></tr><tr><td>

Form Templates

</td><td>

PRB1907844

</td><td>

Reference qualifiers on templates aren't supported on Service Operations Workspace \(SOW\)

</td></tr><tr><td>

Form Templates

</td><td>

PRB1925876

</td><td>

The 'Undo' and 'Cancel' buttons display the same word \(Annuler\) when translated to French

</td></tr><tr><td>

GlideAggregate API

</td><td>

PRB1934853

</td><td>

'Pivot Table' data visualization in domain doesn't show sys\_choice label with 'inactive=false' when 'glide.sys.domain.use\_record\_domain\_for\_choice\_list' is true

</td></tr><tr><td>

GlideAggregate API

</td><td>

PRB1951351

</td><td>

GlideAggregate returns incorrect results for business calendar with condition on date field

</td></tr><tr><td>

GlideAggregate API

</td><td>

PRB1964202

</td><td>

It is not possible to groupBy a Function field

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

GlideFilter API

</td><td>

PRB1872222

</td><td>

The business rule conditions 'Size bytes' and 'greater than' are not working as expected

</td></tr><tr><td>

GlideRecord

</td><td>

PRB1934284

</td><td>

GlideQuery.parse\(\) throws error for 'Choice' fields with '--None--' selected, while the equivalent GlideRecord encoded query works

</td></tr><tr><td>

GlideRecord

</td><td>

PRB1940425

</td><td>

Users are unable to install the Security Incident Response app due to an exception

</td></tr><tr><td>

GlideRecord

</td><td>

PRB1939111

</td><td>

Long term Fix for OOM issue to enable the DataFabric metric/stats

</td></tr><tr><td>

GlideRecord

</td><td>

PRB1946744

</td><td>

Querying against the 'numeric value' variable silently fails because casting to 'signed' isn't supported in postgres

</td></tr><tr><td>

GlideRecord

</td><td>

PRB1962118

</td><td>

Prevent 'Floating Point Number' fields from being created with a max length of 7 or less

</td></tr><tr><td>

GlideRecord

</td><td>

PRB1769440

</td><td>

GlideQuery isn't escaping '^' characters

</td></tr><tr><td>

GlideRecord

</td><td>

PRB1862257

</td><td>

Column Level Restricted Caller Access can be bypassed by GlideRecord.addExtraField

</td></tr><tr><td>

Glide Server APIs

</td><td>

PRB1946733

</td><td>

setStartDateTime API behavior change for strings passed in

</td></tr><tr><td>

Glide Server APIs

</td><td>

PRB1840576

</td><td>

The portal top page is displayed instead of the edited knowledge article after publishing

</td></tr><tr><td>

Glide Server APIs

</td><td>

PRB1850252

</td><td>

Update\(\) failing when there are other 'Where' clauses besides the primary key are being used for GlideQuery

</td></tr><tr><td>

Glide Server APIs

</td><td>

PRB1885968

</td><td>

The 'Change records', 'Show Matching', and 'Filter Out' options no longer work in the Related CI list XML field

</td></tr><tr><td>

GraphQL API

</td><td>

PRB1900136

</td><td>

The validation of reference fields in the GraphQL schema is inefficient/expensive and adds latency

</td></tr><tr><td>

GraphQL API

</td><td>

PRB1971431

</td><td>

Extremely large tables are queried from GlideRecordSchema, causing out of memory errors

</td></tr><tr><td>

GraphQL API

</td><td>

PRB1927998

</td><td>

Session messages are not rendered in List Views for UI Builder lists

</td></tr><tr><td>

GRC Platform Plugins

</td><td>

PRB1906345

</td><td>

'Revised By' on Knowledge appears blank intermittently when updating article by GRC Policy

</td></tr><tr><td>

GRC Platform Plugins

</td><td>

PRB1924501

</td><td>

Policies have a page break alignment issue

</td></tr><tr><td>

Grouped Rows

</td><td>

PRB1885946

</td><td>

The action 'Back to grouped view' doesn't disappear after restoring the filter to default in a workspace list view or navigating to a different list category

</td></tr><tr><td>

Guided Setup \(Legacy\)

</td><td>

PRB1908191

</td><td>

Screen reader announces the content information in Guided Setup as table

</td></tr><tr><td>

Guided Setup \(Legacy\)

</td><td>

PRB1908971

</td><td>

Insufficient color contrast on text elements in the 'Guided Setup' page

</td></tr><tr><td>

Guided Setup \(Legacy\)

</td><td>

PRB1925947

</td><td>

Semantic issues in Guided Setup screen

</td></tr><tr><td>

Guided Tours

</td><td>

PRB1886549

</td><td>

While saving an incident on Service Operations Workspace \(SOW\), the error 'SOW Canvas Error' appears

</td></tr><tr><td>

Health Log Analytics \(Family\)

</td><td>

PRB1964296

</td><td>

Upgrading Glide after the Health Log Analytics \(HLA\) app was uninstalled will install HLA back

</td></tr><tr><td>

Hermes \(Family\)

</td><td>

PRB1941776

</td><td>

Queue depth comes back &gt; 0, even if there are zero messages

</td></tr><tr><td>

Hermes \(Family\)

</td><td>

PRB1902282

</td><td>

Don't show warning message for 'Cannot find matching namespace, for: '

</td></tr><tr><td>

Hermes \(Family\)

</td><td>

PRB1888169

</td><td>

Unnecessary logging in syslog by KafkaConsumerRegistry and GlideHermesTopicManager

</td></tr><tr><td>

Hermes \(Family\)

</td><td>

PRB1922260

</td><td>

External port test runs when it shouldn't

</td></tr><tr><td>

Hermes \(Family\)

</td><td>

PRB1925871

</td><td>

Instance PKI Certificate Generator is displaying KMF error

</td></tr><tr><td>

History Set

</td><td>

PRB1886989

</td><td>

Selecting the AVIT record history gives the error 'Remediation target date must be in the future.'

</td></tr><tr><td>

Horizon Component Library

</td><td>

PRB1891279

</td><td>

The pop-up message '\[Attachment deleted…\]' is still displayed on workspace after abort deletion by a business rule

</td></tr><tr><td>

Horizon Component Library

</td><td>

PRB1818590

</td><td>

now-pagination-control resets the first page \(page 0\) unnecessarily

</td></tr><tr><td>

Horizon Component Library

</td><td>

PRB1786792

</td><td>

In the GRC Compliance Workspace, automatically detected errors are identified by color alone

</td></tr><tr><td>

Horizon Component Library

</td><td>

PRB1892046

</td><td>

The auto-resize limit doesn't work when the text area is read-only

</td></tr><tr><td>

Horizon Image Component

</td><td>

PRB1910414

</td><td>

Image component configuration panel is missing the Upload button and flow in Platform Analytics Dashboard

</td></tr><tr><td>

Horizontal Portal Capabilities for Customer Service

</td><td>

PRB1918820

</td><td>

Login page sessions should be excluded from guest usage metrics

</td></tr><tr><td>

Horizontal Portal Capabilities for Customer Service

</td><td>

PRB1921775

</td><td>

CSP external user registration failed for password

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1911888

</td><td>

Users with the 'sn\_hr\_core.admin' role and without the 'admin' role are unable to grant the 'sn\_hr\_core.admin' role to other users

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1958041

</td><td>

After Zurich upgrade, LE tasks aren't getting created

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1904008

</td><td>

The description of an HR case for a MRVS drop-down field is set with a value instead of a label

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1919627

</td><td>

When a user who doesn't have an HR admin role updates user segment status, the 'Failed to create user segment' error appears

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1941212

</td><td>

A cross-scope error occurs when opening the 'Request Personal Information Report' HR template

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1936359

</td><td>

Base instance notificationss are missing for some COEs

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1939177

</td><td>

User can't view the attachment on a HR case

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1940348

</td><td>

Users are unable to perform an employee relations case search on the 'Create Case' screen

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1963713

</td><td>

The 'Evidence' table's attachment rename functionality isn't working in HR Agent Workspace

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1965533

</td><td>

There isn't logic to prevent a user from entering 'HR Service' even when the task type isn't 'HR Service'

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1974935

</td><td>

'ER Case Commented \(opened\_for\)' email notification produces an empty short\_description and triggers the error 'Source descriptor is empty while recording access for column task.short\_description'

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1799096

</td><td>

Some tables in HR core are not properly defined in the dictionary, resulting in unexpected behavior

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1899131

</td><td>

User is not able to access ER case when sn\_hr\_er\_involved\_party has an HR case field as 'NULL'

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1902459

</td><td>

Discrepancy in User Count on Bulk Case Request for User Segment Group

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1917275

</td><td>

When sys\_user records is updated, the update is synchronized with a record of sn\_hr\_core\_job.job\_active = false

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1918489

</td><td>

Transfer HR case functionality is not working for system/bot created tickets

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1919962

</td><td>

The tag feature does not work in HRSD cases for non-admin users in HR Agent Workspace

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1920358

</td><td>

Client Script "Auto Fill Assigned To field" is only for the HR case Table not for child tables

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1927289

</td><td>

The user is able to enter a Work Note containing only spaces in the Suspend Dialog Box

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1928882

</td><td>

When loading an HR profile, the employee number field changes on the display

</td></tr><tr><td>

HR Service Delivery Case Management for Lifecycle Events

</td><td>

PRB1915543

</td><td>

Journey shows the incorrect task number to Hiring Manager

</td></tr><tr><td>

HTML Field Type Editor

</td><td>

PRB1918842

</td><td>

Before Query business rule doesn't work correctly after Yokohama Upgrade

</td></tr><tr><td>

HTML Field Type Editor

</td><td>

PRB1933221

</td><td>

Extra space is shown in HTML field when change tab in the form

</td></tr><tr><td>

HTML Field Type Editor

</td><td>

PRB1951698

</td><td>

Videos aren't reproducible in an HTML field after saving a record

</td></tr><tr><td>

HTML Field Type Editor

</td><td>

PRB1961384

</td><td>

A KB article with valid wiki text throws a syntax error for the wiki\_text field, and content isn't rendering anymore: 'Table tags are not properly matched'

</td></tr><tr><td>

HTML Sanitizer

</td><td>

PRB1934851

</td><td>

The HTML Sanitizer incorrectly replaces rel=external with rel=nofollow in HTML dictionary fields

</td></tr><tr><td>

Identification and Reconciliation API

</td><td>

PRB1972817

</td><td>

There's an NMA update exception

</td></tr><tr><td>

Identification and Reconciliation API

</td><td>

PRB1934489

</td><td>

Revisit design of Computer Rule introduced in CMDB CI Class Models version 1.77.1

</td></tr><tr><td>

Identification and Reconciliation API

</td><td>

PRB1848571

</td><td>

Slow SQL observed during Tenable.io Open Vulnerabilities integration, impacting ingestion rate

</td></tr><tr><td>

Identification and Reconciliation API

</td><td>

PRB1912104

</td><td>

CMDB 360 Preview does not show display values for Reference fields

</td></tr><tr><td>

Identification and Reconciliation API

</td><td>

PRB1932467

</td><td>

IRE does not update target table of sys\_object\_source when CI class change happens from a different source

</td></tr><tr><td>

Identity

</td><td>

PRB1890898

</td><td>

UserHasRole PatchJob may inadequately update user role inheritance if it processes a user prior to original transaction \(M2MSlushbucketSaveJob\) completion

</td></tr><tr><td>

Identity

</td><td>

PRB1949855

</td><td>

The "system" user is not allowed to modify scripts because of missing snc\_required\_script\_writer\_permission role

</td></tr><tr><td>

Inbound IP Address Access Control

</td><td>

PRB1918984

</td><td>

IPAddress objects occupying high memory

</td></tr><tr><td>

Inbound IP Address Access Control

</td><td>

PRB1931553

</td><td>

Database connections Pool Exhaustion issue

</td></tr><tr><td>

Incident Communications Management

</td><td>

PRB1956997

</td><td>

A communication task SMS notification only includes 2 levels of users

</td></tr><tr><td>

Incident Communications Management

</td><td>

PRB1912198

</td><td>

Failing requests for integration with Zapier

</td></tr><tr><td>

Incident Management

</td><td>

PRB1966341

</td><td>

The 'Changing cmdb\_ci and resolving incident triggers' check HAM action is selected on an incident business rule when validation properties are set to false

</td></tr><tr><td>

Incident Management

</td><td>

PRB1930370

</td><td>

When both files contain the same information, only one of the two attachments from the interaction gets copied over to the incident record

</td></tr><tr><td>

Incident Management

</td><td>

PRB1938914

</td><td>

In the body of the email notification template the section header text "About this incident" should be designated as a heading 2

</td></tr><tr><td>

Incident Management

</td><td>

PRB1941995

</td><td>

Problem coordinators can't associate closed incidents to problems in Service Operations Workspace \(SOW\) \(incident end\)

</td></tr><tr><td>

Innovation Management

</td><td>

PRB1981597

</td><td>

Delete records from the 'im\_m2m\_idea\_category' table which break the associated idea record Audit history and the Activity Stream

</td></tr><tr><td>

Innovation Management

</td><td>

PRB1399211

</td><td>

The 'Getting Started' module for Idea is broken

</td></tr><tr><td>

Innovation Management

</td><td>

PRB1931268

</td><td>

Comments posted against ideas are not displayed as wrapped text

</td></tr><tr><td>

Instance Data Replication \(IDR\)

</td><td>

PRB1878892

</td><td>

Attachment capture records created, and when returned 'Strategy' is null or has include attachments set to 'false'

</td></tr><tr><td>

Instance Data Replication \(IDR\)

</td><td>

PRB1911193

</td><td>

HTML field replication edge case is broken

</td></tr><tr><td>

Instance Data Replication \(IDR\)

</td><td>

PRB1917780

</td><td>

Shared Key recovery does not happen when attempting to seed

</td></tr><tr><td>

Instance Scan

</td><td>

PRB1927870

</td><td>

Instance Scan excludes inactive records , even when the system property 'glide.scan.base\_system\_records' is enabled

</td></tr><tr><td>

Instance Scan

</td><td>

PRB1942594

</td><td>

Muted findings in Instance Scan continue to impact health score calculations, preventing scores from improving to 100 even when all findings are muted

</td></tr><tr><td>

Instance Scan

</td><td>

PRB1908060

</td><td>

Using 'let' keyword impacts update set scan results

</td></tr><tr><td>

Integration Authentication

</td><td>

PRB1958788

</td><td>

Token-based authentication last\_login\_time isn't updated

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1943215

</td><td>

ua\_ih\_usage tracking displays 'unlicensed' when used with new Workflow Data Fabric \(WDF\) SKUs in Xanadu

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1662083

</td><td>

Retry policy shows wrong 'Next Retry' in Ops View

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1928792

</td><td>

Unable to connect to ServiceNow MCP Server using ServiceNow MCP Client

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1933193

</td><td>

Configuration data is missing in REST step

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1983057

</td><td>

ServiceNow base instance Script Includes with duplicate names \(i.e RestStepMultipartUtil and RestStepFormUrlEncodedUtil\)

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1933358

</td><td>

Non-IH outbound calls are counted as IH Usages, even if this flow doesn't cause the outbound request

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1946989

</td><td>

Async HTTP client does not honor proxy bypass settings

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1964766

</td><td>

Refresh token URL is not directly shown in the Application Registry form

</td></tr><tr><td>

Integration Hub Usage Dashboard

</td><td>

PRB1894079

</td><td>

When an API call is done from jelly code in the HTML field of a UI page, the error 'Prior artifact scope is null in call chain: no thrown error' appears

</td></tr><tr><td>

Investment Portal

</td><td>

PRB1920188

</td><td>

Users can't open or filter users/groups when there are a lot of records in the sys\_user table

</td></tr><tr><td>

Issue Auto Resolution for Virtual Agent

</td><td>

PRB1912537

</td><td>

Task SLA field is visible when configuring Issue Auto Resolution \(IAR\) for HR

</td></tr><tr><td>

Journal Field Types

</td><td>

PRB1926543

</td><td>

No global CRUD ACLs on the sys\_journal\_field table

</td></tr><tr><td>

JVM at Scale

</td><td>

PRB1926518

</td><td>

ArrayIndexOutOfBoundsException on MemoryWatcherThread

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB1948809

</td><td>

The 'Security Customer Actions' page isn't displaying weak certificates with Security Center version 3.1.2

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB1950812

</td><td>

SEK rekey job failures

</td></tr><tr><td>

Knowledge Blocks

</td><td>

PRB1861268

</td><td>

The Used Count of a HR scoped Knowledge article \(i.e. Application 'Human Resources: Core'\) record does not increase upon using it by the attaching it to a HR Case using Now Assist

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1905161

</td><td>

An error appears when creating a knowledge article using a business rule

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1964059

</td><td>

The UX sitemap configuration 'sitemap\_config\_KB' can't generate a sitemap

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1920012

</td><td>

The "Valid to" date deosn't populate correctly on the knowledge record based on the timezone of the end user

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1938335

</td><td>

Query range ACL error appears when viewing a link from article expiry notifications

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1981407

</td><td>

After Zurich, the 'Source task' field for knowledge articles isn't assigned

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1916080

</td><td>

In the Service Portal, the knowledge article title is truncated within the Knowledge breadcrumbs

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1927836

</td><td>

Related articles aren't visible in the 'Related Knowledge Articles' widget

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1938603

</td><td>

The user cannot navigate to anchors within a collapsed accordion when the article is opened from Workspace

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1938882

</td><td>

Base instance ACLs in knowledge management treat gs.getProperty\(\) result as boolean which returns a string and doesn't have any significance if the property is true or false

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1944461

</td><td>

Extra UI elements cause update set errors when migrating the kb\_knowledge form view

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1950179

</td><td>

The 'Knowledge Affected products' widget displays cached data from a previous article

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1953401

</td><td>

In Customer Service Portal, the heading structure isn't correct on the homepage

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1953737

</td><td>

kb\_view displays the 'Edit' button when a role doesn't have permissions to edit

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1957071

</td><td>

The white space of list widgets are incorrect due to an 'empty' widget instance value

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1958717

</td><td>

\\The accessible name does not start with the visible label on the Knowledge Bases combo box

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1966145

</td><td>

In Zurich, when the Knowledge Article is moved from 'Draft' to 'Review', the approval mails are not sent to the approver

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1713546

</td><td>

Performance in getLanguagesToDisplay by removing the Summary table

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1871027

</td><td>

Unable to view or write comments on an article when it's viewed using the preview of 'Related Search Results' on an incident form

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1900979

</td><td>

Knowledge article access is blocked on branded mobile apps

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1905164

</td><td>

Knowledge articles in an HR scope have an out of sync 'helpful' count and 'useful' count

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1917569

</td><td>

When trying to move the "Knowledge Article Helpful" widget on top of "Knowledge Article Content", the results are not as expected

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1920755

</td><td>

Knowledge Articles content does not fit in the portal and requires scrolling to the right

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1921678

</td><td>

Wiki field on Knowledge Blocks is visible on Published Knowledge Blocks

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1929677

</td><td>

There's an issue with the dependent field values in Knowledge Management

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1930451

</td><td>

Ineffective SQL query

</td></tr><tr><td>

KPI Details

</td><td>

PRB1972051

</td><td>

On the 'KPI Details' page, a chart isn't rendering the latest score for indicators with fiscal yearly frequency

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1863364

</td><td>

Sys\_ui\_message shows the wrong translation of 'No' to German 'Keine'

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1883354

</td><td>

In the Swedish language, comments don't show properly in the activity stream

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1945159

</td><td>

When adding an affected CI from the related list in Service Operations Workspace and native UI incident forms, the configuration class search doesn't function correctly when using the Finnish language

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1968320

</td><td>

Tooltips in Virtual Agent icon labels have an extra space for Simplified Chinese and Japanese languages

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1975283

</td><td>

The Japanese sys\_ui\_message on the UI page 'set\_initial\_selection\_criteria' unexpectedly has HTML tags

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1850471

</td><td>

'Build' and 'Design' are translated incorrectly in German for CMDB i18n

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1880128

</td><td>

Finnish translation shows 'Osavaltio' instead of 'Tila' in the State field in Yokohama

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1880908

</td><td>

Translated column label for alm\_asset.location in French has changed after upgrading from Washington DC to Yokohama

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1885028

</td><td>

The ''&amp;nbsp;'' character \(non-breaking space\) introduced in the French language pack breaks Event Management Test Connector UI page

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1910767

</td><td>

The question\_choice field is displaying 'um' instead of 'A' for the Brazilian Portuguese language

</td></tr><tr><td>

Legacy Agent Workspace

</td><td>

PRB1937106

</td><td>

Declarative action exclusion doesn't work with table + view combination

</td></tr><tr><td>

Legacy Agent Workspace

</td><td>

PRB1926675

</td><td>

The 360 Record information button doesn't display consistently on the sidebar in CSM workspace without refreshing the browser

</td></tr><tr><td>

Legacy Workflow

</td><td>

PRB1955456

</td><td>

Users are unable to publish a workflow in a scoped application

</td></tr><tr><td>

Legacy Workflow

</td><td>

PRB1959429

</td><td>

There's an accessibility contrast issue on the RITM table where some green icons in the stage column don't meet the minimum 3:1 color contrast

</td></tr><tr><td>

License Usage \(Family Channel\)

</td><td>

PRB1835734

</td><td>

Publisher fetch takes 80 Seconds, which exceeds workspace timeout \(30 seconds\)

</td></tr><tr><td>

License Usage \(Family Channel\)

</td><td>

PRB1931731

</td><td>

Non-licensable \(child\) products are listed in the report for "Licensable software products deployed on containers"

</td></tr><tr><td>

Lifecycle Events

</td><td>

PRB1941769

</td><td>

Lifecycle Event approvals intermittently fail to generate

</td></tr><tr><td>

Lifecycle Events

</td><td>

PRB1942195

</td><td>

HR Lifecycle Events resume cases are failing

</td></tr><tr><td>

Lifecycle Events

</td><td>

PRB1956890

</td><td>

User evaluation against audience on activity fails during rescind

</td></tr><tr><td>

Lifecycle Events

</td><td>

PRB1960147

</td><td>

Rescinding a case with workflows causes an error in the logs

</td></tr><tr><td>

Lifecycle Events

</td><td>

PRB1905399

</td><td>

HR Activity field mapping is not working for 'true' and 'false' values

</td></tr><tr><td>

List Administration

</td><td>

PRB1967492

</td><td>

Export fails when the filter is too long in Service Operations Workspace

</td></tr><tr><td>

List Administration

</td><td>

PRB1924348

</td><td>

Column Personalization preferences aren't saved to the appropriate view in case of list page template

</td></tr><tr><td>

List Administration

</td><td>

PRB1943326

</td><td>

Copying data from the workspace list results in additional help text being copied: 'Press and hold Shift then press Enter to edit.'

</td></tr><tr><td>

List Administration

</td><td>

PRB1934171

</td><td>

Group by is not working on some document ID type columns

</td></tr><tr><td>

List Administration

</td><td>

PRB1883062

</td><td>

In UI Builder, the Presentational List component gets refreshed and creates additional code in macroponent

</td></tr><tr><td>

List Administration

</td><td>

PRB1943196

</td><td>

List personalization doesn't work for a list with a view other than SOW in service operations workspace

</td></tr><tr><td>

List Administration

</td><td>

PRB1930125

</td><td>

Workspace list view doesn't show records for non-admin users

</td></tr><tr><td>

List Administration

</td><td>

PRB1889393

</td><td>

Localization is not enabled for fixed filters

</td></tr><tr><td>

List Administration

</td><td>

PRB1903949

</td><td>

Personalizations on an enclosed list in a workspace persist after refreshing, even after restoring to column defaults

</td></tr><tr><td>

List Administration

</td><td>

PRB1935030

</td><td>

Highlighted values have limited width on the initial load of the now-list

</td></tr><tr><td>

List Administration

</td><td>

PRB1919338

</td><td>

Empty state doesn't show up in the presentation list

</td></tr><tr><td>

List Administration

</td><td>

PRB1795998

</td><td>

Page navigation isn't working for 'Group by' on an incident list

</td></tr><tr><td>

List Administration

</td><td>

PRB1944329

</td><td>

Playbook fields' boolean values aren't editable through list for users when the language is anything other than English

</td></tr><tr><td>

List Administration

</td><td>

PRB1897320

</td><td>

Untranslated text in record list bundle personalization options

</td></tr><tr><td>

List Administration

</td><td>

PRB1948024

</td><td>

A reference list endpoint does not retrieve the record count when non-English languages are enabled

</td></tr><tr><td>

List Administration

</td><td>

PRB1882756

</td><td>

When navigating from 'New List' to 'Select columns' in Service Operations Workspace \(SOW\), it is not in alphabetical order

</td></tr><tr><td>

List Administration

</td><td>

PRB1974024

</td><td>

Date time field is not working as expected

</td></tr><tr><td>

List Administration

</td><td>

PRB1933683

</td><td>

List column widths are not persistent when columns are personalized

</td></tr><tr><td>

List Administration

</td><td>

PRB1947366

</td><td>

Condition Builder isn't resetting in a workspace when switching between 2 specific lists

</td></tr><tr><td>

List Administration

</td><td>

PRB1948701

</td><td>

A ServiceNow list appearance is distorted

</td></tr><tr><td>

List Administration

</td><td>

PRB1948956

</td><td>

There's an improper focus order for a copy URL alert

</td></tr><tr><td>

List Administration

</td><td>

PRB1951492

</td><td>

In the list edit view, the user must scroll to access the 'Cancel' and 'Update' UI actions in Zurich CSM workspace

</td></tr><tr><td>

List Administration

</td><td>

PRB1956876

</td><td>

Selection query and UI state mismatch during multi-page navigation and after selecting all operations

</td></tr><tr><td>

List Administration

</td><td>

PRB1957699

</td><td>

Mandatory field doesn't have an error message

</td></tr><tr><td>

List Administration

</td><td>

PRB1957824

</td><td>

A list cell's background color style is different if 'background-color' isn't all lowercase

</td></tr><tr><td>

List Administration

</td><td>

PRB1958261

</td><td>

The UI is broken in CSM/FSM Configurable Workspace and users are unable to create a list

</td></tr><tr><td>

List Administration

</td><td>

PRB1963950

</td><td>

There's an undefined table name when opening a record in the task table list after a live update

</td></tr><tr><td>

List Administration

</td><td>

PRB1972110

</td><td>

Users are unable to search a configuration item by its correlation ID in an 'Outage' form

</td></tr><tr><td>

List Administration

</td><td>

PRB1973022

</td><td>

The 'View records with this tag' link doesn't work in SOW

</td></tr><tr><td>

List Administration

</td><td>

PRB1973546

</td><td>

Highlighted text in PAR dashboards is shifted to the right in Zurich

</td></tr><tr><td>

List Administration

</td><td>

PRB1973868

</td><td>

Bug in configurable workspace in search reference pop up when editing a list

</td></tr><tr><td>

List Administration

</td><td>

PRB1977162

</td><td>

Duplicate entries on Related list after upgrading Yokohama

</td></tr><tr><td>

List Administration

</td><td>

PRB1842481

</td><td>

TinyURLs are incorrectly generated on compound fields in a Related List

</td></tr><tr><td>

List Administration

</td><td>

PRB1851777

</td><td>

Filter condition in the Predicate builder fails to show the full filter condition after applying a filter

</td></tr><tr><td>

List Administration

</td><td>

PRB1853994

</td><td>

Screen reader fails to announce the number of record information after invoking pagination controls in Dashboards

</td></tr><tr><td>

List Administration

</td><td>

PRB1895808

</td><td>

A URL changes '+' to '%2B', which breaks a 'Favorites' from a keyword search with a space

</td></tr><tr><td>

List Administration

</td><td>

PRB1897982

</td><td>

Unable to remove grouping when the default 'Group By' is applied in the presentational list

</td></tr><tr><td>

List Administration

</td><td>

PRB1898529

</td><td>

Attachment preview is not working when replying through email in the 'Preview record' page

</td></tr><tr><td>

List Administration

</td><td>

PRB1902695

</td><td>

There are duplicate calls noted for nowRecordListConnectedSnapshot on the HomePage load after the perfintegrations build

</td></tr><tr><td>

List Administration

</td><td>

PRB1903361

</td><td>

Lists 'Clear' button is appears hardcoded for i18n

</td></tr><tr><td>

List Administration

</td><td>

PRB1912513

</td><td>

Filtering Choice fields on the list does not work on the parent table list view

</td></tr><tr><td>

List Administration

</td><td>

PRB1915162

</td><td>

List column values have different font sizes in NS-Sonic-Workspace

</td></tr><tr><td>

List Administration

</td><td>

PRB1916589

</td><td>

"No data to display" is not translated on SOW the first time, and only works after a page refresh

</td></tr><tr><td>

List Administration

</td><td>

PRB1916592

</td><td>

An assigning tag containing apostrophe ' adds the "undefined" tag

</td></tr><tr><td>

List Administration

</td><td>

PRB1923987

</td><td>

Unable to edit dot-walked choice fields and remove commas from the display

</td></tr><tr><td>

List Administration

</td><td>

PRB1925183

</td><td>

Save Filter clears out the filter parameters in the URL

</td></tr><tr><td>

List Administration

</td><td>

PRB1926404

</td><td>

The sys\_dictionary attribute isn't honored on integer value on the 'Presentation List' component, which is part of 'Record List Bundle' of UI Builder

</td></tr><tr><td>

List Administration

</td><td>

PRB1926700

</td><td>

Users are unable to select a custom component of a presentational list inside a modal

</td></tr><tr><td>

List Administration

</td><td>

PRB1928221

</td><td>

Table Filter Condition does not give the appropriate results in the list view

</td></tr><tr><td>

List Administration

</td><td>

PRB1929250

</td><td>

A unique name is not defined for the Filter column elements in the list table

</td></tr><tr><td>

List Controller

</td><td>

PRB1953139

</td><td>

'My Lists' sharing doesn't display all the users in a shared option

</td></tr><tr><td>

List Controller

</td><td>

PRB1923677

</td><td>

The wrong record count is rendered when Record Count Limit is enabled

</td></tr><tr><td>

List Controller

</td><td>

PRB1964511

</td><td>

'My Projects' list view in Project Workspace experiences intermittent loading issues

</td></tr><tr><td>

List Controller

</td><td>

PRB1936225

</td><td>

Grouping doesn't work on a group

</td></tr><tr><td>

List Controller

</td><td>

PRB1946318

</td><td>

List doesn't refresh after adding columns via 'Personalize' fields

</td></tr><tr><td>

List Controller

</td><td>

PRB1965637

</td><td>

ACLs are not functioning as expected with data condition getMyExplicitGroups

</td></tr><tr><td>

List Editor

</td><td>

PRB1687900

</td><td>

Users are unable to edit the class in the list view of Service Operations Workspace

</td></tr><tr><td>

List Editor

</td><td>

PRB1904112

</td><td>

Inline edit on list reports dont function for time type fields

</td></tr><tr><td>

List Filters

</td><td>

PRB1735519

</td><td>

Duplicate filters are added in the filter list

</td></tr><tr><td>

List Filters

</td><td>

PRB1899953

</td><td>

My List \[sys\_ux\_my\_list\] column field is unable to cater for dot-walking

</td></tr><tr><td>

List Filters

</td><td>

PRB1911228

</td><td>

The assignment group in the list filter isn't populating correctly

</td></tr><tr><td>

List Filters

</td><td>

PRB1921105

</td><td>

Date filter on the Presentational List doesn't work

</td></tr><tr><td>

List Filters

</td><td>

PRB1943971

</td><td>

Unpredictable behavior when column filtering on Presentational time fields

</td></tr><tr><td>

List Filters

</td><td>

PRB1856614

</td><td>

The dot-walk choice field from a child table cannot filter as choice format, but filter as a string in the workspace for Reference lists

</td></tr><tr><td>

List Multi-Field Edit

</td><td>

PRB1857683

</td><td>

Shift-click to select multiple tasks in lists in Service Operations Workspace \(SOW\) is not working

</td></tr><tr><td>

List Search

</td><td>

PRB1919502

</td><td>

In SOW workspace, the list Keyword filter "Clear" button clears more filters than just keywords

</td></tr><tr><td>

List Views

</td><td>

PRB1925678

</td><td>

Can't resize the column for 'List - Simple' on the dashboard when the horizontal scrollbar appears

</td></tr><tr><td>

List Views

</td><td>

PRB1963196

</td><td>

With a Zurich upgrade, the 'select all' option on the UI Builder list component has moved from left to center

</td></tr><tr><td>

Localization Framework

</td><td>

PRB1915365

</td><td>

Custom font is not available for translations in the Edit Translation page while requesting adhoc translation for Service Catalog items

</td></tr><tr><td>

Major Incident Management

</td><td>

PRB1915124

</td><td>

Selected groups don't show up in the list to send a meeting invite

</td></tr><tr><td>

Major Incident Management

</td><td>

PRB1947195

</td><td>

The 'fav' icon is overidden by the ServiceNow icon in a few ITSM UI pages

</td></tr><tr><td>

Major Incident Management

</td><td>

PRB1960650

</td><td>

Slow SQL query on multiple instances when executing the "ContactManagementEngine.java\#L210"

</td></tr><tr><td>

Major Incident Management

</td><td>

PRB1876477

</td><td>

Choices in the 'Resolution Code' field are visible in other domains

</td></tr><tr><td>

Major Incident Management

</td><td>

PRB1931736

</td><td>

Optimize the business rule \(BR\) 'Attach Communication Plan'

</td></tr><tr><td>

MetricBase

</td><td>

PRB1989962

</td><td>

Metricbase load spikes can cause bursts of server connection errors: 'No threads are available'

</td></tr><tr><td>

Metric Intelligence \(Family\)

</td><td>

PRB1875150

</td><td>

The 'Update CI Tracker' business rule on m2ci causes delays during mass metric registration

</td></tr><tr><td>

MFA with SSO

</td><td>

PRB1907685

</td><td>

Purpose of the link is not descriptive for accessibility

</td></tr><tr><td>

MID Server

</td><td>

PRB1892926

</td><td>

MID connection pools leak sessions when java.lang.Error is thrown while attempting to create connection

</td></tr><tr><td>

MID Server

</td><td>

PRB1942577

</td><td>

MID Server with a closing parenthesis in the Windows service name doesn't start itself after upgrading

</td></tr><tr><td>

MID Server

</td><td>

PRB1909983

</td><td>

Issue with Discovery via WinRM where non-admin MID Server Service users don't have access to get trusted host

</td></tr><tr><td>

MID Server

</td><td>

PRB1966095

</td><td>

Auto MID selection causes excessive metrics to accumulate when connection issues occur

</td></tr><tr><td>

MID Server

</td><td>

PRB1862165

</td><td>

Customer is unable to use DZDO if 'mid.sa.ssh.use\_sncssh' is set to true; it always defaults to SUDO

</td></tr><tr><td>

MID Server

</td><td>

PRB1923181

</td><td>

Agent failover to additional MID servers takes an excessive amount of time

</td></tr><tr><td>

MID Server

</td><td>

PRB1903937

</td><td>

Azure Key Vault Cred resolver is unable to use Managed Identity if MID is configured with proxy

</td></tr><tr><td>

MID Server

</td><td>

PRB1940087

</td><td>

When installing MID on Linux server, the 'agent/configure.sh: line 466: \[: too many arguments' error is shown when enabling Certificate Revocation

</td></tr><tr><td>

MID Server

</td><td>

PRB1925363

</td><td>

Legacy 'Windows Installed Software' probe can't collect software installs due to different format in the output of WMI Runner

</td></tr><tr><td>

MID Server

</td><td>

PRB1943949

</td><td>

Detect or trim the preceding whitespace in MID server installer for an instance URL field

</td></tr><tr><td>

MID Server

</td><td>

PRB1961305

</td><td>

MID Server logs populate into the 'Agent Files' related list instead of 'Agent logs'

</td></tr><tr><td>

MID Server

</td><td>

PRB1964711

</td><td>

Reverse DNS lookup fails due to a mismatch between a fixed FQDN and a dynamically assigned IP address

</td></tr><tr><td>

MID Server

</td><td>

PRB1971195

</td><td>

Events aren't created through the MID Server post-Zurich upgrade due to a weak password in the previous instance

</td></tr><tr><td>

MID Server

</td><td>

PRB1971767

</td><td>

Agent Client Collector policies aren't synced to agents after MID restart and agent reconnection

</td></tr><tr><td>

MID Server

</td><td>

PRB1893043

</td><td>

When triggering a check execution from the instance, MID response encounters a null pointer exception if it does not receive the agent OS version from keepalive

</td></tr><tr><td>

MID Server

</td><td>

PRB1893857

</td><td>

mTLS enabled MID Server failed to start if mid.ssl.bootstrap.default.check\_cert\_chain set to 'false'

</td></tr><tr><td>

MID Server

</td><td>

PRB1898579

</td><td>

When adding Azure to MID Server 'Capabilities' the record is created correctly, but isn't properly linking to the ecc\_agent\_capability table

</td></tr><tr><td>

MID Server

</td><td>

PRB1902328

</td><td>

ACC-F Agent upgrade from instance fails due to directory traversal detected in ResourceCacher.java

</td></tr><tr><td>

MID Server

</td><td>

PRB1904023

</td><td>

The business rule 'Prevent creating duplicate vault' does not exclude the current record during updates, causing it to falsely detect a duplicate

</td></tr><tr><td>

MID Server

</td><td>

PRB1905158

</td><td>

Discovery fails using SSH Private Key credential with Cyberark

</td></tr><tr><td>

Mobile Experience for Field Service Management

</td><td>

PRB1924604

</td><td>

Questionnaires with multiple levels of dependencies display incorrectly on Mobile

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1804416

</td><td>

Inconsistency in which field types from a card template can be changed on the actual card configuration

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1951413

</td><td>

Search cards based on external content can't be configured on fields created on the external content table

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1965358

</td><td>

Scripted screen questionnaire dependencies between fields stop working because of irrelevant evaluations using toString\(\)

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1930548

</td><td>

OfflineGlideRecord.get throws an exception because a generated SQL has mismatched table names

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1940079

</td><td>

Add condition operators to support IN and MATCH\_RGX with the field value in the UI rule

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1950570

</td><td>

Mobile doesn't return all results when searching for French terms when this works correctly on the platform

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1955836

</td><td>

In offline mode, the task list scrolls infinitely

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1988272

</td><td>

Users can only select the Clip icon to upload attachment on Now Mobile MESP Catalog Item web view in Zurich

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1906516

</td><td>

On Mobile iOS, a list scrolls down infinitely

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1911660

</td><td>

Support Record field name in the UI Rule condition on v1 header

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1916821

</td><td>

The prefetch logic for the parameter screen is broken when using scripted variables

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1918106

</td><td>

In the glideDate.ts in parseDateString function,parsing fails when the day ends with '0'

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1925283

</td><td>

Searches in mobile do not create an entry in sys\_search\_event if no results are returned

</td></tr><tr><td>

Multi-factor Authentication \(MFA\)

</td><td>

PRB1902646

</td><td>

MFA SMS Message is not translated correctly

</td></tr><tr><td>

Multi-factor Authentication \(MFA\)

</td><td>

PRB1910692

</td><td>

Issue with MFA Authentication where user is unexpectedly redirected to the /welcome.do page

</td></tr><tr><td>

Multi-factor Authentication \(MFA\)

</td><td>

PRB1931056

</td><td>

In the MFA dasboard, 'Helps you configure MFA...the Yokohama release' should be of type TRANSLATION\_LITERAL so that it can be exposed for translation, instead of type JSON\_LITERAL

</td></tr><tr><td>

Multi-provider Single Sign-on \(SSO\)

</td><td>

PRB1920554

</td><td>

The 'Check certificate expiration' job fails daily

</td></tr><tr><td>

Natural Language Query \(Family Release\)

</td><td>

PRB1992648

</td><td>

com.snc.nlq.MetadataGenerator modifies GlideElement objects in TableDescriptorCache

</td></tr><tr><td>

Next Experience All Menu

</td><td>

PRB1904388

</td><td>

The order of sys\_ux\_registry\_m2m\_category is not working as expected

</td></tr><tr><td>

Next Experience UI16 Theming

</td><td>

PRB1956988

</td><td>

The email window doesn't open in the black theme even after selection of the black theme for the instance

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1897388

</td><td>

A content page fails to load via a module after an upgrade to Yokohama

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1948768

</td><td>

In the Zurich release, switching to the classic application manager displays a blank page

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1945540

</td><td>

The 'Enable Analytics' preference property isn't passing the user\_consent property

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1956585

</td><td>

There's no CSS hook for hover text color for categories within the filter navigator

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1953563

</td><td>

The font doesn't revert after turning off 'Compact'

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1980286

</td><td>

The preference menu freezes when there's a circular dependency in the theme record

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1981408

</td><td>

The Next Experience toggle within the user preferences no longer refreshes the page

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1849930

</td><td>

Referer is none while accessing an external site from the App module

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1905386

</td><td>

When a custom Unified Navigation menu is created, the menu items added in the menu are duplicated in 'All'

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1907056

</td><td>

Approvals showing on Next Experience landing page don't work for non-task table related approvals

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1908544

</td><td>

Default theme is not working when user-criteria is enabled

</td></tr><tr><td>

Next Experience User Menu

</td><td>

PRB1926920

</td><td>

On instances with AI Agents, some users can't be found on the impersonation list

</td></tr><tr><td>

Normalization Data Services

</td><td>

PRB1931854

</td><td>

A core company isn't handled correctly for a domain-separated environment

</td></tr><tr><td>

Notifications for Service Creator

</td><td>

PRB1919705

</td><td>

Catalog service records are not displayed with in the favorites page for specific users

</td></tr><tr><td>

Notify

</td><td>

PRB1942047

</td><td>

Zoom error scenarios should be handled gracefully

</td></tr><tr><td>

Now Actions messaging app for Slack

</td><td>

PRB1934867

</td><td>

Slack Auth Error on 'messaging\_application' JSON configuration change

</td></tr><tr><td>

Now User Experience

</td><td>

PRB1959318

</td><td>

Upgrade doesn't changw fields from 'string' -&gt; 'translated\_field'

</td></tr><tr><td>

Now User Experience

</td><td>

PRB1765528

</td><td>

The sys\_ui\_macro override may be ignored if a similarly named macro is inactive

</td></tr><tr><td>

Now User Experience

</td><td>

PRB1889651

</td><td>

Directly navigating to a list page from the App Navigator in UI16 will trigger multiple '/table\_name\_list.do' transactions

</td></tr><tr><td>

OAuth

</td><td>

PRB1946383

</td><td>

A system property isn't set as intended, causing email account connection failures

</td></tr><tr><td>

OAuth

</td><td>

PRB1923549

</td><td>

OAuth/ID token auth profile authorization doesn't update last\_login\_time

</td></tr><tr><td>

OAuth

</td><td>

PRB1923548

</td><td>

Web Service Only user last\_login and last\_login\_time are updated

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1982308

</td><td>

On-call message number records aren't deleted when a user responds

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1938628

</td><td>

When adding a coverage to a shift, the user is displayed two times on the 'day' view of the on-call schedule

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1923493

</td><td>

Unable to add or edit events from the schedule calendar view

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1981295

</td><td>

OnCallRotation.getPrimaryUser returns null when there's no members on a roster and only coverage present

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1921160

</td><td>

Make necessary changes to support the older behavior for customers who are still using message\_number field on notify\_message table

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1933203

</td><td>

Start of On-Call Schedule does not respect timezone

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1933521

</td><td>

While creating a new shift for group where there exists a shift already that does not overlap with newly one being created, the system throws an error "Span overlaps rotation schedule"

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1939445

</td><td>

workflow.notification is triggered for SMS notify

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1945462

</td><td>

getSpans\(\) returns an empty group\_id

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1945817

</td><td>

An incorrect assignment timestamp generates in the activity stream when using on-call scheduling

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1948234

</td><td>

In the 'On-Call: Escalations By Email Per Rota' workflow, an incorrect user is referenced in an email body when multiple recipients are configured

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1967407

</td><td>

Rosters aren't tagged to on-call shift properly for a few on-call schedules

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1967490

</td><td>

OnCallRotation.getPrimaryUser returns null for across day shift time while using 2024\_schedule\_engine

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1975908

</td><td>

On-call spans internal cache causing issues on the on-call calendar

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1976318

</td><td>

Duplicate incorrect records on table "v\_st\_on\_call\_shifts\_and\_coverages\_my\_team" for on-call group

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1909337

</td><td>

No response after selecting On-Call Calendar if there's no shift in cmn\_rota

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1914307

</td><td>

A user with rejected time-off request cannot provide the coverage for overlapping shifts

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1923652

</td><td>

Meeting end time issue on CAB meeting refresh

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1932044

</td><td>

Overlapping shifts, where one shift lacks a custom escalation setup empty, is resulting in duplicate on-call notifications

</td></tr><tr><td>

OneExtend

</td><td>

PRB1923618

</td><td>

There's a heap OutOfMemory error and node restart in an ITSM use case for Agentic AI Benchmark

</td></tr><tr><td>

OneExtend

</td><td>

PRB1949710

</td><td>

There's an error: 'Failed to get skill config for skillConfigId: 047dbe24434131100b7b5586bab8f25d, capabilityId: while running LLM Based API'

</td></tr><tr><td>

OneExtend

</td><td>

PRB1973586

</td><td>

A newly changed LLM provider setting is reset after upgrading

</td></tr><tr><td>

OneExtend

</td><td>

PRB1920363

</td><td>

checkLLMModelAvailability returns false when the user's preference language isn't English

</td></tr><tr><td>

OneExtend

</td><td>

PRB1959140

</td><td>

IHUB Spoke Util Pack \(com.snc.ihub\_spoke\_util\_pack\) plugin breaks after upgrading Yokohama

</td></tr><tr><td>

OneExtend

</td><td>

PRB1940748

</td><td>

Changed the Active field to false in 'Run script include as FDIH subflow' to keep it hidden

</td></tr><tr><td>

OneExtend

</td><td>

PRB1962281

</td><td>

Users are unable to uninstall a Store application that contains any tables which are restricted as a part of AccessHandler

</td></tr><tr><td>

OneExtend

</td><td>

PRB1980887

</td><td>

Syslog table is flooded with the message 'Neha SNCDEBUG inside LogAIStats action if block'

</td></tr><tr><td>

OneExtend

</td><td>

PRB1929447

</td><td>

Must increase prompt size to 40k

</td></tr><tr><td>

Oracle Reconciliation

</td><td>

PRB1876511

</td><td>

An install shouldn't be deleted if there are applications pointing to it

</td></tr><tr><td>

Oracle Reconciliation

</td><td>

PRB1941470

</td><td>

Oracle Options are marked as 'Unlicensed' even though CAL Records and NUP Entitlements are present

</td></tr><tr><td>

Password Reset

</td><td>

PRB1949370

</td><td>

'Password Reset Error UI' page generates a script error

</td></tr><tr><td>

Password Reset

</td><td>

PRB1917005

</td><td>

Redirection doesn't work in case of password reset email URL

</td></tr><tr><td>

Password Reset

</td><td>

PRB1939021

</td><td>

Security questions in Password Reset \(via Virtual Agent\) are not randomized

</td></tr><tr><td>

Password Reset

</td><td>

PRB1946757

</td><td>

Issues with the first time login registration process and redirection for external users

</td></tr><tr><td>

Password Reset Widget for Service Portal

</td><td>

PRB1938892

</td><td>

Change Password does not honor the property "password\_reset.request.max\_attempt\_window"

</td></tr><tr><td>

PDF Generation

</td><td>

PRB1959833

</td><td>

Header and footer fetches the default type in the report PDF

</td></tr><tr><td>

PDF Generation

</td><td>

PRB1827843

</td><td>

PDF has missing list attributes when a user exports to PDF from a large filter

</td></tr><tr><td>

PDF Generation

</td><td>

PRB1939589

</td><td>

Left header image and right header image do not work correctly in Yokohama release

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1937240

</td><td>

The reports and PA widgets are displayed in the Migration Center without the bulk migration being triggered

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1967641

</td><td>

Errors in the system log are observed with the message '\#DASHBOARD\_INSIGHT\_SERVICE: Error building uuid:XXXXX'

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1914980

</td><td>

Error in the base instance dashboard with the plugin 'Performance Analytics - Context Sensitive Analytics for Change Management'

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1919230

</td><td>

Date Picker shows the error 'Invalid date. Must be a valid date in the format MMM DD YYYY' while trying to select any date

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1823066

</td><td>

Investigate and fix test failures in ams-analytics-business-calendar test project

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1948103

</td><td>

After upgrading from Xanadu to Yokohama, the line chart appearance changes for the 'current year vs. last year' comparison report using data sets

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1963190

</td><td>

Drilldowns from Single Score visualizations with monthly aggregation redirect to the current month instead of the month that the data represents

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1914338

</td><td>

Platform analytics score cards do not look the same after upgrade to Yokohama

</td></tr><tr><td>

Performance Analytics Breakdowns

</td><td>

PRB1930573

</td><td>

Related Lists conditions on a breakdown source do not get applied

</td></tr><tr><td>

Performance Analytics Dashboards

</td><td>

PRB1968325

</td><td>

Translated dashboard tab name reverts to English after refresh

</td></tr><tr><td>

Performance Analytics Dashboards

</td><td>

PRB1954107

</td><td>

Using a session context for prop binding to get a user ID doesn't function with early evaluation

</td></tr><tr><td>

Performance Analytics Dashboards

</td><td>

PRB1832437

</td><td>

The count for DASHBOARD\_LAYOUT jumps significantly upon page refresh

</td></tr><tr><td>

Performance Analytics Widgets

</td><td>

PRB1967553

</td><td>

The Platform Analytics \(PA\) widget 'Word Cloud' only displays the current period \(on load\) and stops responding when selecting other periods

</td></tr><tr><td>

Platform Analytics Component API

</td><td>

PRB1984668

</td><td>

There's a column filter issue in the Data Visualization library page, in which the 'Does Not contain' isn't working on the 'Owner' column

</td></tr><tr><td>

Platform Analytics Component API

</td><td>

PRB1941595

</td><td>

Dashboard categories aren't filtering the dashboards in the Platform Analytics dashboard overview

</td></tr><tr><td>

Platform Analytics Component API

</td><td>

PRB1936517

</td><td>

A user with minimal roles can't add a breakdown to an indicator

</td></tr><tr><td>

Platform Analytics Component API

</td><td>

PRB1961233

</td><td>

Filtering does not support '%' and '\_' symbols

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1977527

</td><td>

columnLimit has an invalid value, as it expected a value than can be converted to type 'Int' but it was a 'String'

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1947499

</td><td>

Editing in two browser tabs results in tabs content mismatch

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1936902

</td><td>

Saving changes to Library is not working as expected in the Platform Analytics Dashboard

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1971556

</td><td>

Rich text components in the in-line dashboard editor are getting partially translated

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1954949

</td><td>

Dashboard is duplicated when first opening if the user is in different domain

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1954828

</td><td>

As a dashboard owner without the admin role, the user cannot set the Owner Group field of a dashboard

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1946249

</td><td>

User with the 'snc\_external' role is unable to see choice values for filters in a Performance Analytics Reporting \(PAR\) dashboard

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1965731

</td><td>

Changes to par\_visualization\_permission aren't captured in sys\_update\_xml

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1908412

</td><td>

Platform Analytics Dashboard translation problem

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1923526

</td><td>

Chart titles are not translated to other languages if the 'sys\_ui\_message' entry has any value in the 'code' field

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB1900864

</td><td>

Filter loads the same string entry multiple times

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB1968556

</td><td>

Users are unable to filter on the sys\_class\_name column of the kb\_knowledge table in a new Platform Analytics dashboard

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB1972756

</td><td>

When adding a filter to a dashboard, the data source doesn't appear until changes are made

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB1832298

</td><td>

Selecting 'Today' does not update the calendar with the user selection

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB1890194

</td><td>

Dashboard filters are not working as expected for cmdb\_admin

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB1907093

</td><td>

There's a change in behavior after upgrading to Yokohama for non-admins when filtering a list when table/data source is a DB view

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB1917204

</td><td>

Translation does not work on 'Filter Group'

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1936887

</td><td>

Dashboard redirection is incorrect for the user if the dashboard is migrated from the library by admin/analytics manager and not activated

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1899127

</td><td>

Some BT1 users can see the migration banner even if they are not the dashboard owners

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1905573

</td><td>

The migrated spline time series with drilldown doesn't work inside PAE dashboard but works in viz designer

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1971216

</td><td>

Guided setup needs a new URL with an updated dashboard ID

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1956520

</td><td>

Support the migration of a tab name and dashboard name translations

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1935002

</td><td>

When upgrading to Yokohama, the initial screen shows the 'Start moving' button in the Migration Center

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1943751

</td><td>

Auto-migration that runs on an upgrade needs a new sysID on each famlily release

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1962944

</td><td>

Duplicate records are created in the analytics\_category\_m2m table when using UnloadDashboard before and after Platform Analytics migration

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1910729

</td><td>

Setting the property com.glide.par.coreui\_single\_migration.enabled to false causes the message 'Cannot migrate icon' to display

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1917338

</td><td>

Translation of Static Content on a core UI dashboard is lost after migrating to a Platform analytics dashboard in Yokohama

</td></tr><tr><td>

Platform Licensing

</td><td>

PRB1894641

</td><td>

Update the SMV1 reference to use the SMV2 reference during installation of remote applications

</td></tr><tr><td>

Platform Licensing

</td><td>

PRB1838592

</td><td>

The allotment type of custom table is removed automatically after the upgrade and migration

</td></tr><tr><td>

Platform Licensing

</td><td>

PRB1965760

</td><td>

The ua\_instance\_state table isn't updating due to an API failure

</td></tr><tr><td>

Platform Runtime

</td><td>

PRB1913417

</td><td>

The StructuredShutdown doesn't wait for the external shutdown to complete

</td></tr><tr><td>

Platform Runtime

</td><td>

PRB1952655

</td><td>

Prevent inserting empty macronames into the sys\_allowlist\_macro\_template table

</td></tr><tr><td>

Platform Runtime

</td><td>

PRB1788007

</td><td>

GlideRecord. getUniqueValue\(\) called from the 'Database' view returns 'null'

</td></tr><tr><td>

Platform Runtime

</td><td>

PRB1913014

</td><td>

GlideChoiceList returns different Dependent field data for different users with different languages

</td></tr><tr><td>

Playbook Experience Core

</td><td>

PRB1965373

</td><td>

When adding an optional activity on a playbook more than once, the playbook bugs

</td></tr><tr><td>

Playbooks \(Family Channel\)

</td><td>

PRB1936766

</td><td>

Playbook properties don't auto-select after a guided setup upgrade or re-publish

</td></tr><tr><td>

Playbooks \(Family Channel\)

</td><td>

PRB1949708

</td><td>

Stage or activity conditions don't work when referring to a playbook input value

</td></tr><tr><td>

Playbooks \(Family Channel\)

</td><td>

PRB1917556

</td><td>

The user observes a 'No Playbook stages available' error in the 'Playbook' tab

</td></tr><tr><td>

Playbooks \(Family Channel\)

</td><td>

PRB1922316

</td><td>

After upgrading to Xanadu, playbook stages/activities disappear from the screen

</td></tr><tr><td>

Predictive Intelligence

</td><td>

PRB1892456

</td><td>

Workflow predictions fail when the attachment is missing for word vector corpus in the ml\_model\_artifact table

</td></tr><tr><td>

Problem Management

</td><td>

PRB1930428

</td><td>

Problem coordinators can't associate closed incidents to problems in Service Operations Workspace \(SOW\)

</td></tr><tr><td>

Problem Management

</td><td>

PRB1952187

</td><td>

Users are unable to create problem tasks

</td></tr><tr><td>

Problem Management

</td><td>

PRB1946370

</td><td>

Problems that are accepted as 'risk' move to 'resolved' as expected, but if they are accepted as 'complete', then the stage changes to 'fix applied due to UI Action'

</td></tr><tr><td>

Process Mining

</td><td>

PRB1912315

</td><td>

Filter set models are calculated on an incorrect number of cases when filter set conditions match more than 10k results

</td></tr><tr><td>

Process Mining

</td><td>

PRB1951278

</td><td>

Uppercase sys\_ids for cases break the log collection

</td></tr><tr><td>

Process Mining

</td><td>

PRB1954737

</td><td>

If a filter is on a large table, filtering in a breakdown definition can cause performance issues

</td></tr><tr><td>

Process Mining

</td><td>

PRB1905387

</td><td>

Addition of Query ACLs in Process Mining

</td></tr><tr><td>

Process Mining

</td><td>

PRB1920054

</td><td>

Conditions with transitions are failing when viewing the 'Schedule task' results

</td></tr><tr><td>

Process Mining

</td><td>

PRB1921496

</td><td>

The scheduled task name is reset to default if its renamed when the task is processed on Glide

</td></tr><tr><td>

Procurement

</td><td>

PRB1971378

</td><td>

The 'Cost' field for purchase order line items populates with incorrect decimal values for the 'kr' currency

</td></tr><tr><td>

Procurement

</td><td>

PRB1933237

</td><td>

Sourcing does not validate creation of TO/PO and incorrectly closes the task

</td></tr><tr><td>

Procurement

</td><td>

PRB1931415

</td><td>

Receive UI action takes a long time to load when the user has a high amount of stockrooms

</td></tr><tr><td>

Project Management

</td><td>

PRB1951811

</td><td>

When the user creates a project with a template, the system inserts all stakeholders defined in the table dmn\_stakeholder\_register without portfolio

</td></tr><tr><td>

Project Management

</td><td>

PRB1918462

</td><td>

The system throws an error and a Resource Allocation record isn't created upon creation of a Resource Assignment record on a project task

</td></tr><tr><td>

Project Management

</td><td>

PRB1907309

</td><td>

Issue accessing a project or demand via the 'Open Project' button on the Investment Portal

</td></tr><tr><td>

Project Management

</td><td>

PRB1936374

</td><td>

The choices for 'Cost Type' are shown in English, even if you set the language preference to Japanese

</td></tr><tr><td>

Project Management

</td><td>

PRB1906764

</td><td>

Unable to set operator for 'Percent Complete' filter in Project Workspace

</td></tr><tr><td>

Project Management

</td><td>

PRB1938591

</td><td>

Deleting a Parent Project Task with a Child Project Task does not record the Child Project Task in Audit Deleted Records \(sys\_audit\_delete\) and Rollback Sequences \(sys\_rollback\_sequence\) in Project Workspace

</td></tr><tr><td>

Project Management

</td><td>

PRB1974918

</td><td>

Key milestones for sub-projects aren't visible on a status report

</td></tr><tr><td>

Project Management

</td><td>

PRB1961178

</td><td>

Copy Partial Project fails silently due to Scheduling Conflicts

</td></tr><tr><td>

Project Management

</td><td>

PRB1941521

</td><td>

Task type breakdowns have incorrect rolled-up actuals when the 'Budget allocation attribute' property is set to 'cost\_type'

</td></tr><tr><td>

Project Management

</td><td>

PRB1943581

</td><td>

An error message appears when creating a project from demand

</td></tr><tr><td>

Project Management

</td><td>

PRB1943677

</td><td>

Project Tasks are created in the Domain of the Domain Picker instead of the Top Project, when a Project Task is created using 'Insert a new row' on the Related List of a Project Form

</td></tr><tr><td>

Project Management

</td><td>

PRB1943681

</td><td>

Project tasks are created in the domain of the domain picker instead of the top project

</td></tr><tr><td>

Project Management

</td><td>

PRB1943685

</td><td>

Requirements are created in the domain of the domain picker instead of the top project

</td></tr><tr><td>

Project Management

</td><td>

PRB1944540

</td><td>

RIDAC records are created/converted in the domain of the domain picker instead of the top project

</td></tr><tr><td>

Project Management

</td><td>

PRB1944646

</td><td>

Shortening a cost plan creates inconsistent numbers

</td></tr><tr><td>

Project Management

</td><td>

PRB1948028

</td><td>

Moving Sub Projects in New Project Workspace is not possible

</td></tr><tr><td>

Project Management

</td><td>

PRB1948080

</td><td>

There's a file error when exporting to Excel from Planning Console

</td></tr><tr><td>

Project Management

</td><td>

PRB1949452

</td><td>

Generating a cost plan link in the Project Workspace &gt; Classical Project Workspace &gt; Financial tab doesn't work

</td></tr><tr><td>

Project Management

</td><td>

PRB1950944

</td><td>

Users with a project manager role see the year '1970' when moving the state to 'Closed Complete' on a project task

</td></tr><tr><td>

Project Management

</td><td>

PRB1951861

</td><td>

Users can't attach a portfolio to a program in a workspace

</td></tr><tr><td>

Project Management

</td><td>

PRB1955983

</td><td>

Project status reports 'Export to Powerpoint' isn't working as expected for $\{project\_key\_milestone\_baseline.end\_date\}

</td></tr><tr><td>

Project Management

</td><td>

PRB1959373

</td><td>

There's a typo in the 'ProjectWorkbenchPhaseValidationAndUpdate' business rule

</td></tr><tr><td>

Project Management

</td><td>

PRB1961018

</td><td>

The planned end date calculation on a project is incorrect when the schedule entry uses ':45' or partial hours

</td></tr><tr><td>

Project Management

</td><td>

PRB1962134

</td><td>

The project task status logic seems to be incorrect due to the script include 'PlannedTaskStatus'

</td></tr><tr><td>

Project Management

</td><td>

PRB1962243

</td><td>

There's a 'PPM Unable to Recalculate Task' error on a project task update

</td></tr><tr><td>

Project Management

</td><td>

PRB1965229

</td><td>

The 'Apply Template' UI action on the planning console displays the following error message 'An error occurred while applying the template'

</td></tr><tr><td>

Project Management

</td><td>

PRB1972438

</td><td>

There's an incorrect rollup of costs in demand currency to demand and task breakdown levels

</td></tr><tr><td>

Project Management

</td><td>

PRB1977018

</td><td>

"Benefit in project currency" retains the old value when the entered benefit is set to "0"

</td></tr><tr><td>

Project Management

</td><td>

PRB1861882

</td><td>

Changing the 'Planned end date' field on Program table \(pm\_program\) and selecting 'Save automatically' moves the Time field by one hour

</td></tr><tr><td>

Project Management

</td><td>

PRB1877352

</td><td>

The 'Assigned to' and 'Additional assignee list' fields are cleared out when mpp files are imported

</td></tr><tr><td>

Project Management

</td><td>

PRB1891228

</td><td>

Excessive/unnecessary events created during 50k/hr order processing test

</td></tr><tr><td>

Project Management

</td><td>

PRB1908085

</td><td>

Error on 'Manage View'

</td></tr><tr><td>

Project Management

</td><td>

PRB1910762

</td><td>

Duplicate widgets are created in the PMO dashboard 'Actuals' tab after upgrading to Yokohama

</td></tr><tr><td>

Project Management

</td><td>

PRB1911900

</td><td>

When planned task rollup is set to 'False' for the column like 'State' and 'Percent' for the Project task table, the parent task 'State' and 'Percent' complete fields are not editable on the Project tasks forms

</td></tr><tr><td>

Project Management

</td><td>

PRB1916682

</td><td>

When a project with a requirement is assigned as a sub-project to another project, the top task for the requirement is not updated

</td></tr><tr><td>

Project Management

</td><td>

PRB1920461

</td><td>

"Start fiscal period" and "End fiscal period" are not update when project task is created before project start date

</td></tr><tr><td>

Project Management

</td><td>

PRB1920544

</td><td>

The "Check It Out" button displays 'Page not found' error for projects that are converted from demand

</td></tr><tr><td>

Project Management

</td><td>

PRB1927590

</td><td>

Error 'Invalid query detected, stack trace below \[Unknown field active in table fm\_expense\_line\] Query \[active=true\]' when selecting 'View expense lines' from Project Workspace

</td></tr><tr><td>

Record Watcher

</td><td>

PRB1956568

</td><td>

Record Watcher doesn't match records when there's a trailing space in the record

</td></tr><tr><td>

Related List Action Model

</td><td>

PRB1890337

</td><td>

A related list action is incorrectly turned off when defining a condition on a parent record field

</td></tr><tr><td>

Related Lists

</td><td>

PRB1936061

</td><td>

GlideElement miscast causes an error in the workspace

</td></tr><tr><td>

Related Lists

</td><td>

PRB1787443

</td><td>

The floating horizontal scrollbar on the related list isn't floating with Next Experience turned on

</td></tr><tr><td>

ReleaseOps - Family

</td><td>

PRB1960603

</td><td>

Deal Registration \(DR\) is not the catching preview conflict in Test, and moves to Ready for Deployment

</td></tr><tr><td>

Reporting

</td><td>

PRB1891029

</td><td>

When a filter condition is applied and the user tries to export the PDF, the filter condition isn't considered and all the records in Yokohama are exported

</td></tr><tr><td>

Reporting

</td><td>

PRB1941537

</td><td>

In Oracle DB instances, report stats can overflow Integer and logs error messages

</td></tr><tr><td>

Reporting

</td><td>

PRB1890706

</td><td>

Double aggregate on a column with the length greater than 30 characters references the display value, not the sys ID

</td></tr><tr><td>

Reporting

</td><td>

PRB1900311

</td><td>

Multi-pivot report drills down to empty list

</td></tr><tr><td>

Reporting

</td><td>

PRB1911390

</td><td>

Country mapping is not working correctly in Reports when performing in a user language that is non-English

</td></tr><tr><td>

Reporting

</td><td>

PRB1913670

</td><td>

Semi-donut chart is not displaying information when users select the dark theme

</td></tr><tr><td>

Resource Management

</td><td>

PRB1904672

</td><td>

In RMW, the resource assignment is not reflected under the user without refreshing

</td></tr><tr><td>

Resource Management

</td><td>

PRB1976554

</td><td>

When a demand with resource assignments is reverted to a draft, the resource allocation is deleted and the resource plan state is updated to 'Planning'

</td></tr><tr><td>

Resource Management

</td><td>

PRB1948165

</td><td>

Resource Assignment doesn't change from 'Pending' to 'Approved' for 'Percent Capacity' effort type \(%\)

</td></tr><tr><td>

Resource Management

</td><td>

PRB1943893

</td><td>

Deleting a project task results in orphaned resource\_aggregate\_monthly records

</td></tr><tr><td>

Resource Management

</td><td>

PRB1964329

</td><td>

All resource assignments aren't visible in the time card 'Resource Assignment' column when one value is selected

</td></tr><tr><td>

Resource Management

</td><td>

PRB1969650

</td><td>

The 'Resource Planned Cost' field in the project task isn't updated when the planned cost in the related resource plan is modified using the rate override option and resource rate

</td></tr><tr><td>

Resource Management

</td><td>

PRB1973105

</td><td>

Planned costs in demand currency and confirmed/allocated costs in demand currency aren't updated on a resource plan

</td></tr><tr><td>

Resource Management

</td><td>

PRB1906312

</td><td>

The 'Resource Assignment' tab is not present on the SPW for the teamspace2 planning table

</td></tr><tr><td>

Resource Management

</td><td>

PRB1920118

</td><td>

Allocated hours do not match requested hours

</td></tr><tr><td>

Resource Management

</td><td>

PRB1927816

</td><td>

Resource Aggregates Monthly do not match with the Resource Aggregates Daily when the resource schedule changes post allocations

</td></tr><tr><td>

Resource Management

</td><td>

PRB1932950

</td><td>

RCA record is not present in the Human Resources Core scope for Employee Profile UI Action record

</td></tr><tr><td>

REST API Framework

</td><td>

PRB1933015

</td><td>

Generated OpenAPI specification file has servers URL with trailing slash causing problems with some tools

</td></tr><tr><td>

RESTMessageV2 API

</td><td>

PRB1934341

</td><td>

RESTMessageV2 executeAsync is unable to refresh token when using in a scoped app's business rule

</td></tr><tr><td>

Restricted Caller Access \(RCA\)

</td><td>

PRB1927893

</td><td>

getDisplayValue\("name\_of\_document\_id\_field"\) returns null when the document\_id isn't set

</td></tr><tr><td>

Restricted Caller Access \(RCA\)

</td><td>

PRB1962158

</td><td>

RCA warning pops up even if there is a valid scope to scope RCA

</td></tr><tr><td>

Restricted Caller Access \(RCA\)

</td><td>

PRB1925925

</td><td>

Users are unable to see the sparkle icon for an email recommendation

</td></tr><tr><td>

Roles

</td><td>

PRB1893348

</td><td>

Deleting a sys\_user\_group with roles fails to update/remove all the roles from the group's members

</td></tr><tr><td>

Rollback Contexts

</td><td>

PRB1942654

</td><td>

'Clean Expired Rollback Contexts' job runs for an extended duration

</td></tr><tr><td>

Scheduled Jobs

</td><td>

PRB1970221

</td><td>

sys\_trigger query latency causes scheduler mutex timeouts and job claim failures

</td></tr><tr><td>

Schedule Optimization

</td><td>

PRB1940536

</td><td>

When an wm\_intraday\_events record is created without an affected record, the related flow errors

</td></tr><tr><td>

Schedules

</td><td>

PRB1868862

</td><td>

Changing glide.sys.time\_format from HH:MM:SS to HH:MM affects the tasks with an end time of 23:59

</td></tr><tr><td>

Schedules

</td><td>

PRB1947840

</td><td>

In 'Schedule calendar', time doesn't work properly if the system uses an AM/PM time format

</td></tr><tr><td>

Script Actions

</td><td>

PRB1911719

</td><td>

Parsing issues detected in the Package Call Removal utility tool

</td></tr><tr><td>

Script Debugger API

</td><td>

PRB1965114

</td><td>

Users can't re-open a script debugger window after closing it

</td></tr><tr><td>

Search Administration

</td><td>

PRB1942924

</td><td>

In HR Workspace, the string 'Keywords' appears hardcoded

</td></tr><tr><td>

Search Administration

</td><td>

PRB1902764

</td><td>

In Global Search Exact Match, selecting 'Go to list view' leads to an error, 'The page you are looking for could not be found' when using any Non-English language

</td></tr><tr><td>

Search Application Configurations

</td><td>

PRB1949837

</td><td>

Search\_application\_admin role grants write access to sys\_dictionary through personalize\_dictionary role

</td></tr><tr><td>

Search Application Configurations

</td><td>

PRB1912254

</td><td>

Performance test results for the E2E backend query show high response results

</td></tr><tr><td>

Search Signals

</td><td>

PRB1982588

</td><td>

The Genius results field is returning empty results \(\{''results'':\[\]\}\) for certain search queries captured in the sys\_search\_signal\_event table, even though the search itself is executed

</td></tr><tr><td>

Search Suggestions

</td><td>

PRB1848010

</td><td>

The screen reader reads out the entire list of items in the Reference field dropdown list, which is too much detail for users to process

</td></tr><tr><td>

Security Attributes

</td><td>

PRB1852325

</td><td>

GlideSecurityManager. dotWalkQueryConditionToBuild QueryElementToGRMap expands dot-walked fields unnecessarily

</td></tr><tr><td>

Security Attributes

</td><td>

PRB1930543

</td><td>

Assignment to "answer" not allowed in security attribute scripts when script is running in strict mode

</td></tr><tr><td>

Security Data Filters

</td><td>

PRB1929955

</td><td>

404 error appears after selecting 'Analyze Performance' when Polaris is turned off

</td></tr><tr><td>

Seismic Framework

</td><td>

PRB1909660

</td><td>

GraphQL query caching issues when the instance is domain separated and when properties are toggled off

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1917134

</td><td>

Data isn't populated in Tuning cards and there's an error on the Checks page 'Sandbox: using sn\_i18n is restricted!'

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1895613

</td><td>

There's different behavior in the JSUtil.isEmpty function after the upgrade from Washington to Yokohama

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1908371

</td><td>

Outbound REST requests with no request body or attachment fail on the base instance RESTclient business rule

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1915039

</td><td>

Regex fails with 'Invalid quantifier ?: com.glide. rest.domain. ServiceException: Invalid quantifier ?'

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1955078

</td><td>

Singletons are broken by the inclusion of a module ID in URI

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1960493

</td><td>

Regexp regression in invalid unicode sequences

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1962399

</td><td>

\\P and \\p escapes are reported as invalid in non-unicode regexps

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1966601

</td><td>

Dot format time \(hh.mm.ss\) doesn't work in Postgres DB

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1976787

</td><td>

Scoped script include with private function thrown when called from same scope

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1989147

</td><td>

Unauthenticated URLs that include invalid URL encoding may redirect to a blank page

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1850260

</td><td>

Script debugger skips to the end of script when stepping over ''gr.insert\(\)'' or ''gr.update\(\)''

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1886474

</td><td>

Users aren't able to turn off the ES toggle for an existing record

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1886555

</td><td>

The 'Select User Role' popup appears when the 'Mobile Callable' field is missing in the script include form

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1925368

</td><td>

Incorrect miss ratio for syscache\_expression

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1968830

</td><td>

Custom approval doesn't move RITM to 'Cancel' when all approvals are canceled for Service Fulfillment Steps

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1935961

</td><td>

Change 'va\_render\_type' from a calculated to a static field

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1909584

</td><td>

Latency issues in AI Search on portal

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1897960

</td><td>

The prices for catalog items on employee center are shown differently depending on if the user is browsing or searching

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1927340

</td><td>

Variable Widget Summarizer throwing $rootScope:infdig error in console

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1917582

</td><td>

Exporting records from the list view of sc\_cat\_item results in more records than what is seen on list view

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1921146

</td><td>

Issue with service catalog order\_now API

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1977677

</td><td>

The event 'Request generated' is not being triggered after using the Catalog item in Mobile variant

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1976031

</td><td>

The lookup select box variable with 'Choices depend on' stores a choice value instead of a label

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1950677

</td><td>

Post Zurich upgrade, masked 'String' fields show the encrypted value

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1781388

</td><td>

There's no padding on forms after switching to Hebrew language

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1606619

</td><td>

In a Service Portal catalog item's form, changing the value of any field then logging out triggers 'Leave site?' and 'Leave page?' confirmation modals

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1936877

</td><td>

"Request Translation" UI Action doesn't work as expected

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1884207

</td><td>

gForm methods-getLabelOf, setLabelOf are not working in platform

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1890520

</td><td>

Image display issue with the 'Catalog Item' component in UI Builder

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1959858

</td><td>

The dropdown list menu value is not populating with Service Catalog

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1938326

</td><td>

When changing the date format to other than yyyy-MM-DD the flow is throwing error "The value for the mandatory field &lt;Duration type&gt; is empty or invalid" in Submit Catalog Item request action

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1949974

</td><td>

Duplicates are created when users double/triple click a standard change item out of a catalog

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1958962

</td><td>

Catalog Builder generates two update sets for the items where 'Not available For' is captured in an empty update set

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1959132

</td><td>

There's slowness in task load

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1976199

</td><td>

The 'Required Information' buttons are missing roles for accessibility

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1977134

</td><td>

Documentation displays conflicting information regarding AI Search and Meta fields

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1977676

</td><td>

Variables are not wrapping correctly on CSM workspace when question length is large in Single Line Text

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1981972

</td><td>

The customized default value of sc\_cat\_item.sc\_catalogs is overwritten after Zurich

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1833466

</td><td>

A warning is not displayed after editing a submitted RITM's multi-row variable set \(MRVS\) and leaving the RITM without saving the changes

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1879491

</td><td>

Screenreader is reading columns incorrectly, and does not match what is seen on screen visually

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1910117

</td><td>

Multi-select default values do not populate a field in the right way

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1915841

</td><td>

Topics are not copied to a new Catalog item from the Copy UI action

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1917416

</td><td>

The user can't horizontal scroll on Variable Instructions images in Mobile

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1920651

</td><td>

Numeric Scale is overflowing from the frame and radio options are hidden in a variable editor on an RITM

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1921073

</td><td>

Migration script "Migrate 3DES" data could run multiple times during upgrade

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1928421

</td><td>

Multiple attachments on a form cause the clean-up process to delete the wrong attachments due to asynchronous processing

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1929699

</td><td>

In Virtual Agent a hyperlink shows as: a href = "sp" target = "blank"

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1932764

</td><td>

The checkbox price label doesn't honor the fixed, single, calculated setting on price field

</td></tr><tr><td>

Service Catalog API

</td><td>

PRB1946265

</td><td>

The Service Builder module gives an 'Invalid Request' error after ATF test

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB1937677

</td><td>

Record producer with reference question gets stuck in Publishing when the referenced table is deleted, and no error is thrown by sn\_sc.CatalogItemVersioningService.publish\(\)

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB1962431

</td><td>

Catalog Builder modifies variable sets when they aren't wrapped properly by formatters

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB1977985

</td><td>

Editable for submitter in Catalog item templates

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB1889322

</td><td>

Heading level 1 on the 'Welcome to Catalog Builder page' is not WCAG 2.4.6 conformity

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB1912643

</td><td>

Issue with Create/Update catalog item with non-English language in Catalog Builder

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB1916832

</td><td>

Record producer does not save an image

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB1924283

</td><td>

Annotation image attachment is not attached as Attachments of the variable

</td></tr><tr><td>

Service Catalog Components

</td><td>

PRB1918551

</td><td>

g\_form doesn't trigger UI re-render when used in the callback function of async \(GlideAjax \) on Workspace

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1952900

</td><td>

Selecting the 'Back' button after saving a record in the variable editor prompts the user to save again

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1933178

</td><td>

The portal screen reader does not announce the 'You do not have any requests' message automatically on the 'My Requests' page

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1936177

</td><td>

Clone Request option on ESC portal redirects users to /sp portal

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1937930

</td><td>

The widget 'SP Category Page' is updated twice, getting double refreshed

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1947153

</td><td>

The lookup select box with a reference qualifier in MRVS displays incorrect labels on the 'SC Catalog Item' widget

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1952792

</td><td>

In Supplier Portal, a visual label isn't announced by a screen reader

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1957018

</td><td>

CSS styling/variable behavior issues in Zurich

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1957355

</td><td>

'No matches found' isn't translated to the user's session language on the 'SC Categories' widget

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1968576

</td><td>

A lookup select box doesn't load values, causing its width to reduce when selected in the portal

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1975164

</td><td>

Universal Task creation doesn't display the 'Requested For' variable from the parent Universal Request

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1976088

</td><td>

When saving an item as a draft, the my\_request widget throws many console errors

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1887916

</td><td>

Slowness is observed when the user select certain variables on a catalog item on Service portal

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1902541

</td><td>

'MRVS Delete row' will focus on the first MRVS instead of the MRVS that the row deleted

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1916587

</td><td>

Focusable content should have tabindex='-1' or be removed from the Document Object Model \(DOM\)

</td></tr><tr><td>

Service Catalog Variables

</td><td>

PRB1913710

</td><td>

There's a cache for the catalog variable default value

</td></tr><tr><td>

Service Creator

</td><td>

PRB1979124

</td><td>

The 'Service Task Processing' flow triggers and sets an assignment differently than a deprecated workflow

</td></tr><tr><td>

Service Level Management

</td><td>

PRB1931328

</td><td>

On the Service Operations Workspace Incident form, if an SLA definition is in a different domain from the currently selected one, the SLA isn't displayed correctly

</td></tr><tr><td>

Service Level Management

</td><td>

PRB1974948

</td><td>

Identical SLA definitions with reset conditions, only differing in duration, can have incorrect duration set when both reset and go into the pause stage

</td></tr><tr><td>

Service Level Management

</td><td>

PRB1910735

</td><td>

Default SLA Condition is used rather than custom condition\_class on contract\_sla on SLA repair when com.snc.sla.condition\_class.caching.enabled=false

</td></tr><tr><td>

Service Level Management

</td><td>

PRB1926636

</td><td>

When a RITM is created from the catalog, the sc\_req\_item record does not display the 'Request' \(REQ\) number in the activity section

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1785221

</td><td>

'Update svc\_ci\_assoc' and 'Error Counters' run heavy queries on instances with a large amount of application services

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1893301

</td><td>

List layout for sa\_ml\_connection\_suggestion has duplicate position values for the list elements

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1931766

</td><td>

UI action allows 'Insert and Stay' action for cmdb\_ci\_service\_discovered without 'Create' rights

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1938102

</td><td>

Flow Discovery Scheduler doesn't work as expected when the connector schedule and scheduler repeat intervals are the same

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1952657

</td><td>

'Duplicate records found while searching for possible matching endpoints' displays when recreating HTTP Entry Point without an IP

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1959919

</td><td>

The cmdb\_ci\_translation\_rule record is flagged by the CMDB Health Completeness metric due to missing mandatory attributes: 'Source IP' and 'Target IP'

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1730575

</td><td>

Debug of pattern is not working for included CIs when using the ACC Agent

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1885999

</td><td>

Adding TCP entry points to Service with the same IP:port and different location fails

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1886863

</td><td>

The cmdb\_ci\_aws\_datacenter class should be excluded from the recompuation base instance

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1889547

</td><td>

The 'Gather VIP information for creating connections' library creates a TCP endpoint that overwrites custom fields

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1895784

</td><td>

Dynamic CI Group doesn't get updated by the job if the number of CIs is over the limit

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1895805

</td><td>

Discovery map fails to load in host view, causing out of memory \(OOM\)

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1904506

</td><td>

Location feature is not working for AVI LB

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1906898

</td><td>

The limit of CIs is not accurate for SmServiceByTagsUtils.getListOfTaggedCIs

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1910332

</td><td>

DNS Lookup Enhanced throws an exception in case the ipList parameter was missed in the answer from DNS Lookup probe

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1914247

</td><td>

The wrong discovery message in a case IP address is in an inactive status

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1919091

</td><td>

TD discovery has NumberFormatException because a pattern returned multiple ports

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1922240

</td><td>

Action "View CMDB group CIs" is broken when removing "cmdb\_group" field from the dynamic CI group form

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1931472

</td><td>

Memory usage is high with many tag-based services due to createSubLogger

</td></tr><tr><td>

Service Model Foundation

</td><td>

PRB1908477

</td><td>

Base instance business rule 'Sync Service Org's address fields' clears the Latitude field incorrectly

</td></tr><tr><td>

Service Operations Workspace

</td><td>

PRB1956001

</td><td>

Identical page title

</td></tr><tr><td>

Service Portal

</td><td>

PRB1917651

</td><td>

The list collector variable on a catalog item doesn't display correctly when seen on the service portal in Yokohama

</td></tr><tr><td>

Service Portal

</td><td>

PRB1934256

</td><td>

Error message is seen in logs while navigating to the portal

</td></tr><tr><td>

Service Portal

</td><td>

PRB1955719

</td><td>

The base instance widget 'Approval Info' creates duplicate comments in the sysapproval\_approver record when rejecting

</td></tr><tr><td>

Service Portal

</td><td>

PRB1922948

</td><td>

Number of approvals in the service portal header isn't refreshed in real time

</td></tr><tr><td>

Service Portal

</td><td>

PRB1919036

</td><td>

A faceted search widget/Genius result card doesn't have a responsive design and disappears on a mobile browser or a small browser window

</td></tr><tr><td>

Service Portal

</td><td>

PRB1932325

</td><td>

'Show filters' isn't translated in the portal search page

</td></tr><tr><td>

Service Portal

</td><td>

PRB1983857

</td><td>

In Zurich, a user can't input a value/type into a KB knowledge base widget

</td></tr><tr><td>

Service Portal

</td><td>

PRB1950805

</td><td>

In the ESC portal, the 'Skip to chat' link fails to land focus on the 'VA chat' button

</td></tr><tr><td>

Service Portal

</td><td>

PRB1935624

</td><td>

'Hide filters' and 'Clear All' in a facet search aren't properly aligned

</td></tr><tr><td>

Service Portal

</td><td>

PRB1979521

</td><td>

Using the date format 'E yyyy-MM-dd' throws an error in Portal

</td></tr><tr><td>

Service Portal

</td><td>

PRB1943746

</td><td>

Table level UI policies don't work in the Service Portal form when the 'Dictionary' fields are mandatory

</td></tr><tr><td>

Service Portal

</td><td>

PRB1935843

</td><td>

In Windows 11, from any web browsers \(i.e. Chrome or Edge\), two Korean alphabet letters are returned despite a user entering one Korean alphabet letter into a base instance Select box in base instance Service Portal and ESC portal pages

</td></tr><tr><td>

Service Portal

</td><td>

PRB1936655

</td><td>

Widget instance options defect

</td></tr><tr><td>

Service Portal

</td><td>

PRB1943881

</td><td>

In Service Portal, list fields don't respect dependent values

</td></tr><tr><td>

Service Portal

</td><td>

PRB1947686

</td><td>

There's no 'Save changes' message when users select the 'Back' button of a browser for an unsaved form in a portal

</td></tr><tr><td>

Service Portal

</td><td>

PRB1947889

</td><td>

A footer position misplaces when to make a footer fixed

</td></tr><tr><td>

Service Portal

</td><td>

PRB1948141

</td><td>

A user's initials in a header avatar overlap with the profile picture after the upload until the page is refreshed

</td></tr><tr><td>

Service Portal

</td><td>

PRB1950851

</td><td>

A screen reader announces 'Required' in English even after the profile language has been changed to German

</td></tr><tr><td>

Service Portal

</td><td>

PRB1953993

</td><td>

The 'Back' button doesn't work stably after selecting a related list twice

</td></tr><tr><td>

Service Portal

</td><td>

PRB1965943

</td><td>

In Service Portal, the attachment window continues to load when dragging/dropping an opened One Drive file

</td></tr><tr><td>

Service Portal

</td><td>

PRB1968872

</td><td>

A case number isn't displayed on the CSM portal under the 'Notification' menu

</td></tr><tr><td>

Service Portal

</td><td>

PRB1969373

</td><td>

When a user changes the bio in their profile on the Portal, they also see the same bio for all other users

</td></tr><tr><td>

Service Portal

</td><td>

PRB1975755

</td><td>

Hamburger menu options are not keyboard accessible

</td></tr><tr><td>

Service Portal

</td><td>

PRB1980456

</td><td>

The DateTimePicker month and year selection views are marked up incorrectly and can't be accessed via keyboard with NVDA

</td></tr><tr><td>

Service Portal

</td><td>

PRB1982105

</td><td>

'End Live Chat' isn't translated for Now Assist in the Virtual Agent window

</td></tr><tr><td>

Service Portal

</td><td>

PRB1710928

</td><td>

Service Portal and Employee Center 'Skip to ...' focus ring does not universally meet the minimum contrast on all banner color themes

</td></tr><tr><td>

Service Portal

</td><td>

PRB1875961

</td><td>

The 'uploading' message is not announced by the screen reader when adding an attachment in Employee Service Center \(ESC\) and Service Portal portals

</td></tr><tr><td>

Service Portal

</td><td>

PRB1894521

</td><td>

Form field lacks visible a label and relies only on placeholder text \(i.e. 'Add an optional comment' or 'Type your message here'\) in the Activity stream in portals

</td></tr><tr><td>

Service Portal

</td><td>

PRB1896387

</td><td>

Issue Now Mobile App Survey - 'Show More' Button for choice question

</td></tr><tr><td>

Service Portal

</td><td>

PRB1900049

</td><td>

'Turn on ECMAScript 2021 \(ES12\) mode' option does not allow ES12 features on Service Portal Widgets

</td></tr><tr><td>

Service Portal

</td><td>

PRB1900517

</td><td>

The Portal Search box is a rectangle instead of oval with white spaces surrounding it

</td></tr><tr><td>

Service Portal

</td><td>

PRB1901391

</td><td>

The visual label is missing from the 'sn-time-ago' element on the Attachment section in the Service Portal

</td></tr><tr><td>

Service Portal

</td><td>

PRB1908848

</td><td>

g\_form.adddecoration seems to behave differently for list vs. choice types on mobile devices

</td></tr><tr><td>

Service Portal

</td><td>

PRB1909572

</td><td>

Invalid ARIA attribute value 'aria-activedescendant''select2-result-label-81'' on the List Collector type

</td></tr><tr><td>

Service Portal

</td><td>

PRB1910219

</td><td>

Table markup is not defined for the Widget information table in the Widget Diagnostics modal

</td></tr><tr><td>

Service Portal

</td><td>

PRB1911196

</td><td>

The 'Report' sp\_widget on click URL is incorrect when data includes an ampersand \(&amp;\)

</td></tr><tr><td>

Service Portal

</td><td>

PRB1912260

</td><td>

When using a portal URL, the user is not redirected to the expected record after SSO authentication

</td></tr><tr><td>

Service Portal

</td><td>

PRB1915044

</td><td>

Standard ticket header title is not translated

</td></tr><tr><td>

Service Portal

</td><td>

PRB1920953

</td><td>

The browser Back button does not navigate to the previous page \(pagination\) in portal

</td></tr><tr><td>

Service Portal

</td><td>

PRB1921882

</td><td>

A session isn't reset on the portal enhance chat for Dynamic Window

</td></tr><tr><td>

Service Portal

</td><td>

PRB1924527

</td><td>

The text, "Find Answers, Faster, Find the answers you need when you need them", is not visible on the homepage up to 400% browser zoom

</td></tr><tr><td>

Service Portal

</td><td>

PRB1926350

</td><td>

.svg format photos don't work in portal

</td></tr><tr><td>

Service Portal

</td><td>

PRB1926621

</td><td>

Skip links shouldn't jump to breadcrumbs in service portal

</td></tr><tr><td>

Service Portal

</td><td>

PRB1927481

</td><td>

Add error message alert on service portal pop-up give date with space after Hours HH: mm:ss

</td></tr><tr><td>

Service Portal

</td><td>

PRB1931939

</td><td>

Service portal menu items do not scroll on mobile and some are cut off

</td></tr><tr><td>

Service Portal Core Widgets

</td><td>

PRB1951416

</td><td>

The Knowledge Base \(KB\) widget KB doesn't display all language articles

</td></tr><tr><td>

Service Portal Core Widgets

</td><td>

PRB1969194

</td><td>

When loading a page, showing a survey instance with an image to the Portal widget generates attachments every time

</td></tr><tr><td>

Service Portal Core Widgets

</td><td>

PRB1843112

</td><td>

The 'Share' modal on the Social Q&amp;A portal widget isn't responsive in an iOS browser

</td></tr><tr><td>

Service Portfolio Management

</td><td>

PRB1957675

</td><td>

The 'Other tasks' Related List from the 'Service Portfolio Management Premium' package causes slowness

</td></tr><tr><td>

Service Portfolio Management

</td><td>

PRB1941525

</td><td>

Mixed-choice labels with the same value of 'Technical Service' create confusion in the user experience

</td></tr><tr><td>

Service Portfolio Management

</td><td>

PRB1952633

</td><td>

Outage duration displays an additional one hour due to DST if the 'begin' time is Nov 2nd 00:00:00

</td></tr><tr><td>

Session Management

</td><td>

PRB1929529

</td><td>

Unhandled exception occurs when getAttribute is called after Glide session invalidation

</td></tr><tr><td>

Session Management

</td><td>

PRB1880419

</td><td>

IP stored in GlideSession isn't updated when an existing session changes IP address

</td></tr><tr><td>

Session Management

</td><td>

PRB1930353

</td><td>

There's a timezone defect as a result of Glidesession.getUser\(\)

</td></tr><tr><td>

Session Management

</td><td>

PRB1958183

</td><td>

An application throws the error 'The request object has been recycled and is no longer associated with this facade' when a Glide transaction is active and the session is destroyed

</td></tr><tr><td>

Sidebar \(Family Release\)

</td><td>

PRB1931636

</td><td>

Optimize member unread query

</td></tr><tr><td>

Sidebar \(Family Release\)

</td><td>

PRB1971434

</td><td>

On SFS trueup, when users send a message, they get an exception saying that this.threadMembers is null and the message isn't sent

</td></tr><tr><td>

Sidebar \(Family Release\)

</td><td>

PRB1908427

</td><td>

The 'Util' menu keeps loading if there are no conversations yet

</td></tr><tr><td>

Skills Management

</td><td>

PRB1941545

</td><td>

In HR Workspace, the 'Skills' table is a non-translatable type

</td></tr><tr><td>

Skills Management

</td><td>

PRB1956971

</td><td>

Skills without the IIFE template overrides a local variable with the same name

</td></tr><tr><td>

Software Asset Data Import

</td><td>

PRB1930648

</td><td>

An excel row field is not populated for standard import

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1906425

</td><td>

BR 'Build primary key on insert' uses single digit month for January to September to calculate primary key, while Script include 'SAMPSoftwareUsageDataSourceIntegration' uses double digits

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1942745

</td><td>

There's an incorrect 'Active rights' calculation when extending the end date and updating purchase rights in the same update

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1909356

</td><td>

The recon job fails when custom products don't have the 'Publisher' field stamped

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1907339

</td><td>

Value of 'Subscription period' defaults to 'annually' after bulk import of entitlements

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1959756

</td><td>

The 'Connection Setup' section is missing on the Custom Integration view for the Workday Integration Profile after upgrading sn\_sam\_saas\_int

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1965456

</td><td>

An ACL introduced in Zurich blocks users with no role from accessing alm\_entitlement\_user

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1975702

</td><td>

total\_spend/true\_up\_cost/over\_licensed\_amount/potential\_savings values at the publisher level are set to 0 even though Product\_results have those values

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1981043

</td><td>

User resolution rules aren't working if the subscriptions don't have a UPN

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1890559

</td><td>

The scheduled job 'SAM - Update value builder usage' fails with the message, 'Fail' instead of the standard 'Failed' message

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1905727

</td><td>

The samp\_sw\_reclamation\_rule table's last\_activity\_threshold field definition has an incorrect 'Choice' definition

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1915761

</td><td>

An 'Install' table has a cross scope issue since the code is moved to Store

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1919496

</td><td>

Filter options in workspace are not translated

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1920322

</td><td>

On Red Hat, an undetermined reason is caused by an incorrect 'Virtualized By' relationship

</td></tr><tr><td>

Software Asset Management Integration with Citrix

</td><td>

PRB1914340

</td><td>

Error while executing a discovery pattern

</td></tr><tr><td>

Software Asset Management Publisher Pack for Citrix

</td><td>

PRB1869215

</td><td>

Citrix Source installs created from persistent devices

</td></tr><tr><td>

Software Asset Management Publisher Pack for Oracle

</td><td>

PRB1968348

</td><td>

'Licenses Required' and 'Licenses Owned' are shown as empty if the CPU count is missing on a VM instance

</td></tr><tr><td>

Software Asset Management Publisher Pack for Oracle

</td><td>

PRB1897054

</td><td>

In the samp\_oracle\_options table, the column 'Currently Used' needs to be renamed to 'Considered' for licensing

</td></tr><tr><td>

Software Asset Management Publisher Pack for SAP

</td><td>

PRB1856239

</td><td>

Developer NUT users should be licensed separately from a developer environment

</td></tr><tr><td>

Software Asset Management Workspace \(Glide\)

</td><td>

PRB1925065

</td><td>

Software Asset Overview Activity center alerts fetch a failure log for the previous week's run, causing a discrepancy with a successful newer job log

</td></tr><tr><td>

Software Asset Normalization

</td><td>

PRB1847357

</td><td>

Users with the sam\_admin role can't view custom software product and custom software product suggestions lists on License Operations

</td></tr><tr><td>

Software Asset Normalization

</td><td>

PRB1857676

</td><td>

Discovery model's discovered product doesn't match the software install's display name

</td></tr><tr><td>

Software Asset Normalization

</td><td>

PRB1904901

</td><td>

The enhancements for Norm product / publisher are not cleared / stamped on a few installs

</td></tr><tr><td>

Software Asset Reclamation

</td><td>

PRB1916098

</td><td>

SAMPReclamationUtil throws an exception

</td></tr><tr><td>

Software Asset Reclamation

</td><td>

PRB1862254

</td><td>

The 'SG-SCCM' import job deletes a software install with a reclamation candidate

</td></tr><tr><td>

Software Asset Reclamation

</td><td>

PRB1907403

</td><td>

Reclamation candidates and reclamation rule issues

</td></tr><tr><td>

Software Discovery

</td><td>

PRB1579663

</td><td>

File-based discovery populates the version only on the first software install record for a DM

</td></tr><tr><td>

Software Discovery

</td><td>

PRB1958646

</td><td>

Duplicate installs are created from applications

</td></tr><tr><td>

Software Discovery

</td><td>

PRB1967095

</td><td>

Software Asset Connections doesn't set the last scanned on cmdb\_sam\_sw\_install

</td></tr><tr><td>

Software Entitlements

</td><td>

PRB1943125

</td><td>

Total cost calculation in software entitlements for workspace is different than on the form

</td></tr><tr><td>

Software Entitlements

</td><td>

PRB1902573

</td><td>

Business Rule 'Ensure Entitlements do not exceed rights' gets an error when allocate licenses are equal to rights

</td></tr><tr><td>

Software Entitlements

</td><td>

PRB1937440

</td><td>

Agreement type is not available for CrowdStrike license metric group

</td></tr><tr><td>

Software Entitlements

</td><td>

PRB1873270

</td><td>

The 'Copy Allocation' page is unable to select values for reference values using the 'Lookup' icon for the Source Entitlement field in the SAM Workspace

</td></tr><tr><td>

Software Entitlements

</td><td>

PRB1928263

</td><td>

SAM user doesn't have access to copy allocations

</td></tr><tr><td>

Software Models

</td><td>

PRB1902396

</td><td>

Query errors display on a Software Model record due to a client side GlideRecord query

</td></tr><tr><td>

Source Control Engine

</td><td>

PRB1943030

</td><td>

Failed to link to Source Control through MID server

</td></tr><tr><td>

Source Control Engine

</td><td>

PRB1828098

</td><td>

When applying remote changes from the source control using the CCID REST API, a failure in the pre-processing doesn't update the tracker with details about why it failed

</td></tr><tr><td>

Source Control Engine

</td><td>

PRB1899903

</td><td>

Author elective update file is missing for app customization under 'Source control'

</td></tr><tr><td>

Source Control Engine

</td><td>

PRB1923645

</td><td>

Metadata delete records are queried multiple times when commit changes to source control

</td></tr><tr><td>

Standard Ticket Page

</td><td>

PRB1954051

</td><td>

Field states should reflect in the standard ticket summary generation

</td></tr><tr><td>

Standard Ticket Page

</td><td>

PRB1939753

</td><td>

Issue with user mention in additional comments when accents are present

</td></tr><tr><td>

Standard Ticket Page

</td><td>

PRB1969370

</td><td>

There's a random language translation on a request in Portal

</td></tr><tr><td>

Survey Management

</td><td>

PRB1926528

</td><td>

Sentiment Analysis doesn't work on surveys

</td></tr><tr><td>

Syntax Editor

</td><td>

PRB1804517

</td><td>

The field type 'HTML template' on a standard form does not load properly when placed after field type 'Script' or 'Script \(Plain\)'

</td></tr><tr><td>

Syntax Editor

</td><td>

PRB1911045

</td><td>

The sys\_user\_has\_role switches to a guest user when the user session is invalidated

</td></tr><tr><td>

System Archiving

</td><td>

PRB1938103

</td><td>

Reparenting of sys\_attachment doesn't work when the table name is longer than 37 characters

</td></tr><tr><td>

System Events

</td><td>

PRB1943448

</td><td>

There's inconsistencies in event creation due to the gs.eventqueue\(\) method not handling undefined script objects

</td></tr><tr><td>

System Events

</td><td>

PRB1939635

</td><td>

There's a missing 'Partition' column in SysEvent even after a Xanadu upgrade

</td></tr><tr><td>

System Events

</td><td>

PRB1965182

</td><td>

Automate alert deactivation logic and accomodate DST related fixes

</td></tr><tr><td>

System Events

</td><td>

PRB1926794

</td><td>

sysevent records stuck in queued ID state

</td></tr><tr><td>

System Export Sets

</td><td>

PRB1835154

</td><td>

Improve retry logic in POST API from MID server LES Consumer to Customer REST endpoint

</td></tr><tr><td>

System Import Sets

</td><td>

PRB1880984

</td><td>

Attempting to save merged changes on data source entries on sys\_upgrade\_history\_log results in error message

</td></tr><tr><td>

System Import Sets

</td><td>

PRB1972454

</td><td>

Easy import with double byte character sys\_id import attribute values are not able to coalesce

</td></tr><tr><td>

System Notifications

</td><td>

PRB1938027

</td><td>

A new notification makes all other notifications unread in Next Experience

</td></tr><tr><td>

System Notifications

</td><td>

PRB1912721

</td><td>

Rollback context being invalidated by Notification NPE, causing Automatic Test Framework \(ATF\) to not rollback

</td></tr><tr><td>

System Update Sets

</td><td>

PRB1930782

</td><td>

Unintended sys\_ui\_form\_section\(domain = global\) is created when the user commits the update set in another domain

</td></tr><tr><td>

System Update Sets

</td><td>

PRB1934960

</td><td>

Incorrect update set behavior when changing sys\_choice table reference

</td></tr><tr><td>

System Update Sets

</td><td>

PRB1940344

</td><td>

Update sets that contain DELETE for a "parent + child" table don't honor order \(hierarchy of tables\) of deletion when committed

</td></tr><tr><td>

System Update Sets

</td><td>

PRB1961575

</td><td>

'Days of Week' on the update XML Diff UI displays an incorrect day of the week

</td></tr><tr><td>

System Update Sets

</td><td>

PRB1971540

</td><td>

URL bug when viewing the sys\_update\_set\_list table through an Update Set picker

</td></tr><tr><td>

System Update Sets

</td><td>

PRB1885422

</td><td>

Importing an update set of an upgrade plan or items also installs the applications on the instance

</td></tr><tr><td>

System Update Sets

</td><td>

PRB1887979

</td><td>

For update sets including sys\_choice records, the record inserted on the target instance once the update set is committed is incorrect, and has a table that is 'task' when it should be 'incident'

</td></tr><tr><td>

System Update Sets

</td><td>

PRB1891223

</td><td>

Adding an icon on sc\_cat\_item \(sys\_user\_image.do\) leads to out of memory \(OOM\) issues and node restarts

</td></tr><tr><td>

System Update Sets

</td><td>

PRB1895618

</td><td>

The application hyperlink in sys\_ui\_messge 'inform\_user\_about\_ability\_to\_deploy\_customizations\_with\_app\_link' is broken

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1828517

</td><td>

There's an SQL error when inserting invalid or var\_\_ tables as a dependent field for document it

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1757717

</td><td>

addValue \(string field, number value\) isn't working as expected on the 'number' field in the 'sys\_number\_counter' table

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1799203

</td><td>

When a table is created using the Japanese language setting, an error message is displayed

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1638197

</td><td>

Skipping the online alter check doesn't create the field that doesn't require online alter and can use one of the available storage aliases

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1937528

</td><td>

Nesting coalesce\(\) within datediff\(\) for a field function no longer functions in RaptorDB

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1945120

</td><td>

Flow actions are deleted when they are reverted to older versions

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1970189

</td><td>

Updating a sys\_documentation record doesn't update the column label value for the CMDB child table

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1970986

</td><td>

Deleting a field from the 'cmdb\_ci' table doesn't cascade delete the field labels, choices, ACLs, and so on

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1893553

</td><td>

Altering a large table through deletion, field type change, or field length increase times out by a UI quota rule and becomes canceled

</td></tr><tr><td>

Table API

</td><td>

PRB1936930

</td><td>

Loading and saving REST API Access Policies is slow

</td></tr><tr><td>

Table Cleaner

</td><td>

PRB1966084

</td><td>

Cascade delete fails when the table is audited and record serialization fails

</td></tr><tr><td>

Table Cleaner

</td><td>

PRB1929847

</td><td>

Hex Table Cleaner should add "table\_cleaner" category on select queries

</td></tr><tr><td>

Tables and Columns Data Dictionary

</td><td>

PRB1933921

</td><td>

Schema table does not display fields inherited from parent table

</td></tr><tr><td>

Tags

</td><td>

PRB1977490

</td><td>

Deny unless ACL is not working when using tags

</td></tr><tr><td>

Targeted Communications

</td><td>

PRB1934355

</td><td>

Rejecting targeted communication shows an unexpected comment

</td></tr><tr><td>

Telemetry Glide Infrastructure

</td><td>

PRB1920545

</td><td>

CDC replication turns off batch DB update operations on replicated tables, causing increased upgrade times on instances

</td></tr><tr><td>

Template Management for Field Service

</td><td>

PRB1920388

</td><td>

When accessing a work order template, $sm\_templates can be slow and cause memory issues on the client-side \(browser\)

</td></tr><tr><td>

Territory Planning

</td><td>

PRB1894202

</td><td>

While doing 'Agent- relocation', the now-date-time-interval component is showing the error on load: 'The second date/time must match format: yyyy-MM-dd HH:mm:ss'

</td></tr><tr><td>

Time Card Management

</td><td>

PRB1944070

</td><td>

The 'Task' field in time cards are able to be removed by a time card user role who created the time card in the list view

</td></tr><tr><td>

Time Card Management

</td><td>

PRB1890906

</td><td>

Time sheet displays empty space on the bottom of the last time card

</td></tr><tr><td>

Time Card Management

</td><td>

PRB1896237

</td><td>

A negative hour time card update is possible from the timesheet portal form view even when it's blocked in Portal

</td></tr><tr><td>

Time Card Management

</td><td>

PRB1911895

</td><td>

Project Time Category dropdown list box shows the 'None' option multiple times when the list has more than 20 choices

</td></tr><tr><td>

Time Card Management

</td><td>

PRB1923751

</td><td>

Time Card validation intermittently fails for the decimal Max Hours per day

</td></tr><tr><td>

Transaction Management

</td><td>

PRB1966462

</td><td>

FORKED\_TRANSACTIONS shows NaN for semaphore service\_saturation metric in /load\_stat.sdo

</td></tr><tr><td>

Transaction Management

</td><td>

PRB1936264

</td><td>

Transactions aren't removed from TransactionManager because an exception is thrown in the http thread before transaction queuing

</td></tr><tr><td>

Transaction Management

</td><td>

PRB1956071

</td><td>

'Deflater has been closed' error occurs intermittently when finishing gzip stream at the end of a transaction

</td></tr><tr><td>

Transaction Management

</td><td>

PRB1965589

</td><td>

The 'Check DC Supports' TLS job shouldn't run for on prem users

</td></tr><tr><td>

Transaction Management

</td><td>

PRB1913194

</td><td>

Unhandled exceptions in GlideTransactionProcessor may leak HTTPTransaction objects, causing memory issues

</td></tr><tr><td>

UI Actions

</td><td>

PRB1936788

</td><td>

The color field value of a sys\_ux\_form\_action\_layout\_item record is shown in English when the user session language is Japanese

</td></tr><tr><td>

UI Actions

</td><td>

PRB1806248

</td><td>

In the 'Additional Actions' menu in all modules, there is a backslash \(/\) before apostrophe \('\) in the help tag when French Canadian is used

</td></tr><tr><td>

UI Actions

</td><td>

PRB1886211

</td><td>

When a UI action calls an external site via Iframe, the UI action will only fire once

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1974424

</td><td>

There's a tree picker performance issue seen with an assignment group after upgrading to Zurich

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1976103

</td><td>

The glide\_list field with choices in an extension table form \(incident\) shows choices for a parent table \(task\)

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1887661

</td><td>

Records are not being added based on the selected Configuration Class item

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1919959

</td><td>

An exception displays in a syslog when adding/removing a property in a full-screen slushbucket

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1870246

</td><td>

In Service Operations Workspace, the user is unable to add the date in the start and end date fields using numeric input in the change request page under schedule

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1615389

</td><td>

Pause Condition builder doesn't work when 'Update selected option' is chosen from the list view

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1598544

</td><td>

When creating an HR case from an interaction record, 'interaction\_related\_record' duplicates are created

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1924730

</td><td>

The Radio button choice display value is not labeled in platform list

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1936609

</td><td>

Mandatory asterisk is shown on a field with an empty display name

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1937530

</td><td>

Reference fields do not display correctly

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1945187

</td><td>

An @mentions flyout is dismissed after providing a space after matching a user

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1947095

</td><td>

Keyboard focus is lost once the email address is added in the 'Work notes' list under the 'Notes' tab

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1947541

</td><td>

There are AXE violations for the RTE Compose editor

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1955199

</td><td>

After selecting enter on a list field, it loses focus and users can't type another value

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1957375

</td><td>

An attachment rename icon in 'Create Record' and user form activity is displayed even though the user doesn't have access to modify the file name

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1957609

</td><td>

When a 'Timer' field is paused with a value, modifying any other field value changes the display to 00:00:00

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1958960

</td><td>

A username is truncated without an ellipsis in a workspace preferences' flyout when Next Experience is turned off

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1960935

</td><td>

The 'Radio button' field isn't visible and configurable in a new template form

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1962617

</td><td>

The plugin 'now\_assist\_context\_menu from url /scripts/now\_assist\_context\_menu\_tinymce\_plugin.js' failed to load

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1974408

</td><td>

A few error messages are issued multiple times by the screen reader

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1575910

</td><td>

When an 'Activity Stream' pop-up is opened using a mouse, the user can interact with other interactive elements in the main content

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1815398

</td><td>

The recurring price is updated incorrectly

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1822002

</td><td>

Unable to change the user record linking to ar\_sys\_user

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1879698

</td><td>

The NOW\_RECORD\_TIME\#VALUE\_CHANGED event is not fired on UI field interaction

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1887400

</td><td>

The date picker isn't translated to the appropriate locale

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1890158

</td><td>

On the form Reference field, dropdown list custom colors in Next Experience UI are different from the workspace UI

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1893966

</td><td>

The '@mention' function does not initially find the user

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1896321

</td><td>

The 'Time worked' field \(type timer\) auto starts even for closed records in Service Operations Workspace \(SOW\)

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1900926

</td><td>

Heading &lt;h1&gt; is inappropriately defined

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1916843

</td><td>

@mentions shortcuts don't work properly on a form's section

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1917295

</td><td>

A form with an attachment field is broken after an upgrade from Yokohama to Zurich

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1920656

</td><td>

The telephone number in the URL field of External Links is broken

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1926852

</td><td>

'Add file' overlaps with the title in base instance

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1928623

</td><td>

Recent selections do not appear in workspace even after saving the field value multiple times

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1969026

</td><td>

Deferred Related list can fail the UI page ACL if the script condition checks URL parameters

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1912648

</td><td>

The Personalize Form feature for record on workspaces isn't working

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1888357

</td><td>

Cannot invoke 'com.glide.sys.cache.CompactCacheEntry.getBytes\(\)' because 'entry' is null

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1949131

</td><td>

g\_form.getValue\(\) isn't working as expected to get the currency\_type from a 'Currency' type field

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1949349

</td><td>

Form fields overlap in the HTML editor in configurable workspace

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1853423

</td><td>

When the user tries to attach a video greater than 500MB from the HTML field, nothing happens and a console error logged

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1886963

</td><td>

onChange script runs while the form is submitted

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1688241

</td><td>

Broken links to Docs from context-sensitive help

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1918107

</td><td>

Rename option isn't available for published knowledge articles in pop-up

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1972511

</td><td>

Invalid payload event for CTRL\_RECORD\#MACROPONENT\_PROPERTY\_CHANGED

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1939423

</td><td>

Workspace record context is not updating Now Assist Panel \(NAP\) on the initial load of the record

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1833166

</td><td>

Form Sections aren't hiding from non-admin users for FSM work order tasks

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1881480

</td><td>

List2\_related\_lists.xml calls while building syscache\_realform cache when the related list loading is OnDemand

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1861230

</td><td>

When 'glide.ui.fetch.list.record.count.asynchronously' is set to true, the record count never completes in Reference Lookup in Workspaces

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1933227

</td><td>

Failure to upload .jpeg files via .zip file

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1934313

</td><td>

In Workspace, the Default view is not checked in the View section of the Additional actions menu of the form header in non-English languages

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1935372

</td><td>

In Catalog Builder, UXF Notifications are rendered behind the client script or UI policy wizard modal

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1943361

</td><td>

Tasks in the ER flows aren't instantly visible on the case

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1944434

</td><td>

Personalized form fields that are already hidden by ACLs cause a form error

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1945607

</td><td>

Currency edits on workspace list multiform default to USD

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1959255

</td><td>

In SOW, the onChange client script only runs in the workspace if reference isn't there on the layout

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1728612

</td><td>

There's no confirmation message provided to users who update a form field

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1847354

</td><td>

There's no facility for setting the default encryption of attachments to 'None' in the configurable workspace

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1847545

</td><td>

The vertical scrollbar of a browser is gone after closing a second modal

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1884099

</td><td>

g\_form.setValue\(Obj\) on workspace saves a truncated value for the reference field

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1889844

</td><td>

Base instance incident caller location auto-population is not working

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1893371

</td><td>

Keyboard shortcut 'Ctrl + click' for Windows is not working as expected on Service Operations Workspace \(SOW\), and does not open the reference field in a new tab as it doess on Mac OS using 'Cmd + click'

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1897655

</td><td>

g\_form.setSectionDisplay isn't working as expected on the workspace, as it always displays if there's any mandatory field on the section

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1897661

</td><td>

Date validations don't work properly on SOW with 'Current Minute Configuration' in UI policy

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1898889

</td><td>

The 'Upload a file' message on the Attachment side bar doesn't disappear on workspace

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1910382

</td><td>

Hidden fields are saved in the template

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1912124

</td><td>

Unable to use first letter navigation with JAWS for many controls in Form view, buttons and header controls in Incident, on the 'Interaction &amp; Request' page

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1916089

</td><td>

Selecting 'Hide my templates' on UI builder hides all three tabs on Templates panel: All, My Template, favorites.

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1918236

</td><td>

The 'Child Incidents' related list gets populated with all available incidents

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1925140

</td><td>

File Attachment type does not display a label in some edge cases

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1927627

</td><td>

Article template table fields are not shown in the knowledge base field "Set default knowledge field values" which was shown earlier in a Utah version

</td></tr><tr><td>

UI Policies

</td><td>

PRB1769904

</td><td>

onChange is not working as expected for UI Policy

</td></tr><tr><td>

UI Policies

</td><td>

PRB1927901

</td><td>

UI policy actions work as expected on platform but not on workspace, based on "Clear the field value"

</td></tr><tr><td>

Universal Request

</td><td>

PRB1893973

</td><td>

Missing scope specifier in the business rule 'Update Universal Request State' \(e6d26e3673120010888b6238edf6a751\) intermittently fails to update universal request

</td></tr><tr><td>

Upgrade Center

</td><td>

PRB1952534

</td><td>

Upgrade monitor reflects 'Installing Distribution' if the upgrade is triggered twice and 'Upgrade Distribution' has an empty completion time

</td></tr><tr><td>

Upgrade Center

</td><td>

PRB1927990

</td><td>

Full cache flushes occur during on-demand installations/upgrades, causing performance issues

</td></tr><tr><td>

Upgrade History

</td><td>

PRB1940724

</td><td>

onSubmit script error appears when selecting the 'Save merge' button for skipped record in contract\_sla

</td></tr><tr><td>

Upgrade History

</td><td>

PRB1832209

</td><td>

Assignment type doesn't have choices

</td></tr><tr><td>

Upgrade Plans

</td><td>

PRB1904790

</td><td>

Unable to remove the upgrade plan item due to the message, 'Not allowed - unpublished applications or elevated priviledged only plugins are not allowed to be installed via upgrade plan'

</td></tr><tr><td>

Usage Analytics

</td><td>

PRB1963094

</td><td>

Users aren't able to interact with the Unified Navigation menu when the web SDK configuration becomes empty

</td></tr><tr><td>

Usage Analytics

</td><td>

PRB1923784

</td><td>

Console error on the landing page on HR Agent Workspace, 'TypeError: Cannot read properties of undefined \(reading 'set'\)'

</td></tr><tr><td>

Usage Analytics

</td><td>

PRB1966686

</td><td>

There's a heap memory issue due to the queuedevents array growing uncontrollably

</td></tr><tr><td>

Usage Analytics

</td><td>

PRB1982586

</td><td>

Usage Insights SDK Configuration API call fails for non-ISO application names in headers

</td></tr><tr><td>

Usage Analytics

</td><td>

PRB1912033

</td><td>

Definition ID counts in usageanalytics\_count shows negative value \(-6\)​

</td></tr><tr><td>

User Administration

</td><td>

PRB1961641

</td><td>

The snc\_external user can't grant the admin role

</td></tr><tr><td>

User Impersonation

</td><td>

PRB1970709

</td><td>

When impersonating any user, the message '\_SCREEN\_MACROPONENT\_PLACEHOLDER' appears

</td></tr><tr><td>

UX Framework

</td><td>

PRB1968071

</td><td>

Viewport content isn't refreshed if the tab is already selected before saving the record, causing the content in the tab to not populate

</td></tr><tr><td>

UX Framework

</td><td>

PRB1924105

</td><td>

Custom Domain Theme built in theme builder resets to a different color after refreshing the homepage

</td></tr><tr><td>

UX Framework

</td><td>

PRB1966630

</td><td>

Workspace tabs aren't rendering screens

</td></tr><tr><td>

UX Framework

</td><td>

PRB1980248

</td><td>

When hovering over two workspace tabs \(parent or child/secondary\), the tooltip stays on the screen and doesn't disappear

</td></tr><tr><td>

UX Framework

</td><td>

PRB1980696

</td><td>

Workspace interaction logging sends non-JSON 'params' causing server-side JSONException \(UX Metrics\)

</td></tr><tr><td>

UX Framework

</td><td>

PRB1949471

</td><td>

Users can't make the Service Operations Workspace main tab limit to open only one record, even after setting 'maxMainTabLimit' to 1

</td></tr><tr><td>

UX Framework

</td><td>

PRB1947452

</td><td>

UX screen record allows the 'Parent Macroponent' field to be set to the screen within the same screen collection as the current screen record

</td></tr><tr><td>

UX Framework

</td><td>

PRB1957790

</td><td>

An error page displays when adding parameters to a page variant after a Zurich upgrade

</td></tr><tr><td>

UX Framework

</td><td>

PRB1948796

</td><td>

Domain props aren't set on the page macroponent on a domain separated instance

</td></tr><tr><td>

UX Framework

</td><td>

PRB1958053

</td><td>

The macroponent\_config field is unable to store the configured value due to its maxLength limit

</td></tr><tr><td>

UX Framework

</td><td>

PRB1962984

</td><td>

A loading overlay appears underneath the modal post-upgrade to Zurich

</td></tr><tr><td>

UX Framework

</td><td>

PRB1964710

</td><td>

With a modified Workspace App Shell, the SOW page doesn't load on refresh

</td></tr><tr><td>

UX Framework

</td><td>

PRB1971390

</td><td>

Content triggered by hovering-over is not dismissed by using the ESC key

</td></tr><tr><td>

UX Framework

</td><td>

PRB1972320

</td><td>

There's an unexpected focus shift to the first focusable element on a page

</td></tr><tr><td>

UX Framework

</td><td>

PRB1972737

</td><td>

Conditions for displaying page variants aren't working for web embeddable components

</td></tr><tr><td>

UX Framework

</td><td>

PRB1886937

</td><td>

There's an issue with QCO closing out without the 'click' of a mouse

</td></tr><tr><td>

UX Framework

</td><td>

PRB1888822

</td><td>

Keyboard shortcut to close the current working tab quickly without pressing multiple tabs is not present

</td></tr><tr><td>

UX Framework

</td><td>

PRB1892477

</td><td>

Portal App Shell workspace pages jump to the middle of the page on save

</td></tr><tr><td>

UX Framework

</td><td>

PRB1923311

</td><td>

UX dependency tracing should use LargeContentDiskCache.getMetadata to avoid file touching

</td></tr><tr><td>

UX Framework

</td><td>

PRB1925894

</td><td>

Jackson and ux.runtime errors are generated in the logs

</td></tr><tr><td>

Validated Payload Execution

</td><td>

PRB1921311

</td><td>

PayloadHashHandler.calculatePayloadHash\(\) causes an out of memory error on the nodes due to large data streaming from sys\_choice

</td></tr><tr><td>

Versatile Node and Cluster Configuration

</td><td>

PRB1902157

</td><td>

ClusterSynchronizer may overwrite a newer cluster state with an outdated value if message processing takes too long and the state changes during that time

</td></tr><tr><td>

Versioning

</td><td>

PRB1950900

</td><td>

Removing plugin application files from a global application reverts the files to a base version

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1970662

</td><td>

Gemini web search does not work on Yokohama Now Assist and the latest Zurich builds

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1956188

</td><td>

Translation issue on 'View AI Steps'

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1952103

</td><td>

Remove showNoSkillsConfigured options passed when requesting the skill picker control in Now Assist Portal \(NAP\)

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1928402

</td><td>

Virtual Agent enhanced chat translation doesn't work on chat menu items

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1962876

</td><td>

Interaction Record form does not always pop up when receiving an inbound call

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1962077

</td><td>

The Virtual Agent \(VA\) audio beep isn't heard for all chats in Zurich

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1768573

</td><td>

Profanity filter keyword issues

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1937290

</td><td>

The 'New conversation' button disappears when using certain custom branding colors

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1937033

</td><td>

Agent statements containing URLs are not translated for a chat user when DTAC is active

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1915544

</td><td>

The Virtual Agent \(VA\) topic execution returns a tool response instead of a main skill

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1915766

</td><td>

Now Assist search result links aren't configurable by portal on mobile

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1890524

</td><td>

Increase in heap utilization due to expression cache for search

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1960129

</td><td>

A conversation abruptly ends after a cold start conversation with a pre-chat survey enabled

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1918457

</td><td>

Virtual Agent Designer updates captured in the update set can't be committed to the target instance

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1891918

</td><td>

The Now Assist panel displays a misleading notifications indicator

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1966041

</td><td>

Virtual Agent iframe is rendering with a blank screen

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1936798

</td><td>

The scroll bar of the Virtual Agent is no longer visible in Chromium 139/140 versions

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1874005

</td><td>

A record in provider\_user\_map is still inactive, causing Now Virtual Agent to fail approvals

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1973526

</td><td>

The business rule 'VA Phone Interaction - On Close' is not firing in the 'wrap\_up' state

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1939270

</td><td>

Hide the 'Show links for each record' toggle on VA Designer 'Table' bot response

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1894545

</td><td>

LLM responses aren't unmasked if streaming is turned on with a Java proxy enabled

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1934605

</td><td>

The user can't use AI Connector VAD Node to invoke an agent in non-global topics

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1870642

</td><td>

In Now Assist, the chat experience for the greeting / closing message isn't working for non-English languages

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1923131

</td><td>

sn-chat-choice-picker appears instead of text-picker for users that turned on the new sys prop

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1965604

</td><td>

An interaction is moved to 'Closed/abandoned' after a manual reassignment to an offline agent

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1897152

</td><td>

Unexpected badge for an unread notification displays on the chat history icon after loading a citation and navigating back

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1940559

</td><td>

The Virtual Agent topic 'Check Case Status \(Template\)' is stuck at '. . .' in the Virtual Agent chat

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1969087

</td><td>

&amp;para is getting converted to the paragraph symbol in sys\_cs\_conversation

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1925872

</td><td>

Error appears for Dynamic Translation when input text is not passed

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1940858

</td><td>

RITM/REQ isn't mapped to an interaction when a conversational catalog item is submitted

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1971759

</td><td>

NAVA should read the catalog sysid correctly from FDIH invocation

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1895063

</td><td>

Dynamic choice fields are not translated automatically when the requester\_session\_language is set

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1920893

</td><td>

A suggestion message is only displayed in French after English input

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1915102

</td><td>

Post chat survey question is triggered twice

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1945377

</td><td>

'Now Assist Panel - Platform \(default' set up topics have a read-only protection policy

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1939997

</td><td>

Non-actionable notifications in Virtual Agent aren't cleared when load\_active\_only is set to true

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1942164

</td><td>

Interactions closed by timeout are incorrectly marked with 'Left While Search'

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1942868

</td><td>

The user wants an improved experience for the 'View More Records' button

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1949727

</td><td>

The 'Incident' list page fails to display records due to a missing URL encoding of a Base64 query

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1954676

</td><td>

Fallback isn't working for Now Assist Virtual Agent \(NAVA\)

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1958358

</td><td>

VaInputs isn't receiving the correct value from a topic block

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1959241

</td><td>

Virtual Agent shows the message twice for information lookup

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1959445

</td><td>

Now Assist Panel shows 'Unable to load'

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1959534

</td><td>

Virtual Agent is not considering the user's timezone preference on the date/time variable while submitting a catalog item

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1962100

</td><td>

Interactions related to deleted conversations are updated with a 'Unable to generate Transcript' string in transcript fields

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1962199

</td><td>

There's an error retrieving a transcript for a conversation with getMessagesFromTranscript\(\)

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1963459

</td><td>

A conversation abruptly ends after a cold start conversation that has a pre-chat survey turned on

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1970956

</td><td>

Now Assist in Virtual Agent returns incorrect dates/times with certain inputs

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1978377

</td><td>

Tab on the Chat button takes the user to the chat window instead of the input area for accessibility

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1557268

</td><td>

Chat doesn't have a method to provide alternate text for multiple image attachments within a chat session

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1823250

</td><td>

Values to the interaction set from sysparm\_interaction\_&lt;column&gt; overwrites updated values at end of conversation

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1829786

</td><td>

A card response of type 'Small image with text' doesn't display the data on the card in Virtual Agent from Xanadu version

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1832704

</td><td>

In the Virtual Agent chat bot, the 'Minimize chat window' text appearance is different in each instance

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1845885

</td><td>

Ensure &lt;meta name''viewport''&gt; does not disable text scaling and zooming \(meta\[name=''viewport''\]\) for Virtual Agent

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1869171

</td><td>

Virtual Agent Context variable does not work in Virtual Agent Designer for testing

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1888867

</td><td>

Attachment on Virtual Agent \(VA\) shows twice for CSM portal on the requester end

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1889246

</td><td>

When com.glide.cs.advanced-chat.popover is 'true', the chat header doesn't display correctly for Virtual Agent chat branding

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1896976

</td><td>

The 'Start a new conversation' pop-up box in Virtual Agent is out of the screen

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1899038

</td><td>

The bot text response script message is skipped if there is a space in the start of it

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1901893

</td><td>

Toggle to collapse categories on the 'Show Me Everything' page is not working as expected within Virtual Agent

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1902259

</td><td>

'Add as Update Set on Skill Kit' does not work at all for skills that use tool builders because critical records are missing

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1910766

</td><td>

One extend APIs aren't honoring a timeout with Virtual Agent \(VA\)

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1911010

</td><td>

With DTAC enabled and an agent name displaying in the Virtual Agent header, Virtual Agent uses an incorrect name

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1913443

</td><td>

If http call fails with 403/404 etc, it still shows as delivered in sys\_cs\_message for Virtual Agent API

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1918095

</td><td>

Virtual Agent total Chat Bubbles\(notifications\) doesn't clear unread message count when support multiple conversations is enabled

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1918623

</td><td>

Glide node does not reliably start due to a dp\_cache\_refresh\_thread\_name deadlock error

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1919055

</td><td>

Add a new property to to turn off the 'shorten responses' feature by default

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1921731

</td><td>

Post chat survey allows the user to switch topics

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1926973

</td><td>

Links data aren't included in a synthesized response in a transcript

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1927206

</td><td>

Sensitive data for agent chat does not work with URLs

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1930364

</td><td>

AI search fails for users in a sub-domain on a domain separated instance

</td></tr><tr><td>

Virtual Agent Designer Legacy

</td><td>

PRB1917696

</td><td>

Virtual Agent Designer isn't displaying options for subflows if there are more than 100 spokes

</td></tr><tr><td>

Virtual Agent Designer Legacy

</td><td>

PRB1934841

</td><td>

The conversation field is null in an execution plan when invoking an AI agent from the AI connector node

</td></tr><tr><td>

Virtual Agent Designer Legacy

</td><td>

PRB1938160

</td><td>

Card output node error if Virtual Agent can't find valid record

</td></tr><tr><td>

Virtual Agent Designer Legacy

</td><td>

PRB1949979

</td><td>

Unable to pass inputs to AI Agent in Virtual Agent topic using AI Connector utility

</td></tr><tr><td>

Virtual Agent Designer Legacy

</td><td>

PRB1897174

</td><td>

Converting published LLM topics to topic blocks leaves sys\_gen\_ai\_skill records

</td></tr><tr><td>

Virtual Agent Designer Legacy

</td><td>

PRB1928396

</td><td>

Date time input when used in a topic block returns null on output parameters

</td></tr><tr><td>

Virtual Agent third-party integrations

</td><td>

PRB1941102

</td><td>

Typing a response before a previous response has completed can lead to a 'technical error' in the conversation

</td></tr><tr><td>

Virtual Agent third-party integrations

</td><td>

PRB1904755

</td><td>

Exception occurred while getting context profile for conversationId in the error log in the Virtual Agent API

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1906343

</td><td>

The chat window container header isn't following the branding color selected on the 'Assistants - Branding page'

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1948623

</td><td>

Uptake new versions of Unified Experience Framework \(UXF\)

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1922825

</td><td>

The 'New chat' button is in disabled mode after a live agent connection has ended when the chat history is turned off

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1893493

</td><td>

Non-conversational catalog items can't be selected if they are preceded by external KB article citations

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1964982

</td><td>

Web client needs to honor the 'format': 'markdown' in synthesized response

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1925994

</td><td>

Engagement Messenger isn't loading chats after upgrading Yokohama

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1947114

</td><td>

In Virtual Agent, parent questions aren't announced by a screen reader for multiple-choice prompts

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1981038

</td><td>

There's an extra empty message added after the HTML output when messages arrive too quickly

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1930544

</td><td>

Size issue with custom emojis and 'Masked' icon in branding for engagement messenger

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1889678

</td><td>

User can input text before the conversation starts after a Xanadu upgrade

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1933088

</td><td>

Processing loader is displayed even after getting a response

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1933376

</td><td>

Custom protocol links such as kolauncher:// are not rendered to be selected in Virtual Agent Genius responses

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1940975

</td><td>

Support more markdown for text messages and synthesized responses

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1944963

</td><td>

Support more markdown for text messages and synthesized responses

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1947524

</td><td>

In Virtual Agent, topics listing with a '&lt;ul&gt;' are missing a programmatic/accessible label

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1953555

</td><td>

Now Assist panel \(NAP\)/Now Assist Virtual Agent \(NAVA\) Client does not load

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1957770

</td><td>

Streaming is slow or frozen when performing continuous searches within the same conversation for Now Assist Virtual Agent \(NAVA\)

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1963494

</td><td>

The synthesized response isn't displayed completely

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1964923

</td><td>

'There is a JavaScript error in your browser console' errors in the ESC landing page

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1965054

</td><td>

Virtual Agent messages are displayed twice

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1981024

</td><td>

Markdown link \[label\]\(url\) renders an incorrect URL when the URL contains a dollar sign \($\)

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1869729

</td><td>

Choices provided in the picker is dragged below the visible window

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1893104

</td><td>

In Now Assist Multi-Turn Catalog Ordering, the 'Data/Time' type variable isn't showing the current time, but as 00:00AM in Virtual Agent for non-English language mode

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1901501

</td><td>

Having more than one query sysparm does not work in the sn\_va\_web\_client\_login page

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1916685

</td><td>

Scrolling doesn't work in choice-picker intermittently

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1921052

</td><td>

Name is not defined for the Now Assist Virtual Agent button

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1922217

</td><td>

ServiceNowChat.open isn't opening Portable Virutal Agent

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1925903

</td><td>

The user's attachment is sent twice when connected to agent

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1927910

</td><td>

When initiating a chat with Enhanced Chat active in a portal, the '+' button to start a new chat remains disabled after the chat times out

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1931626

</td><td>

Bottom input is enabled in NLU topic block in enhanced chat

</td></tr><tr><td>

Visual Task Boards

</td><td>

PRB1955767

</td><td>

vtb\_card and vtb\_task ACLs cause performance issues if either table is used in a related list

</td></tr><tr><td>

Visual Task Boards

</td><td>

PRB1919994

</td><td>

Performance is heavily impacted when a VTB has a high number of swim lanes

</td></tr><tr><td>

Visual Task Boards

</td><td>

PRB1979360

</td><td>

The 'Manage Filters' button doesn't in the visual task board 'Load Filter' modal

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1965546

</td><td>

In SOW, navigating to location kiosks doesn't return any results

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1967419

</td><td>

Walk-up location schedule isn't working properly post-upgrade to Zurich

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1902465

</td><td>

Scheduled job update happens with the inactive user and creates multiple follow-up appointments

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1954321

</td><td>

A walk-up check in dropdown is partially blocked by an iPad virtual keyboard

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1954978

</td><td>

The 'Walk-up' experience doesn't display any walk up locations due to an error related to Query Range ACLs

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1956906

</td><td>

The user observes an error after creating a walk-up appointment, assigning the appointment to a user and rescheduling the appointment in portal

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1957263

</td><td>

The 'Getting Started' module isn't working under the 'Walk-up Experience' application

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1962829

</td><td>

A walkup user is assigned to the 'Conditional Script Writer' group, which in turn prevents access to the walkup portal

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1968746

</td><td>

The 'Explicit role' plugin should be enabled, assigning the snc\_internal role to a walkup user which has a conditional script writer role

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1974025

</td><td>

Query\_match ACL error for walkup user while user check-in in walkup experience

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1981055

</td><td>

Image on the 'Walk up reservation' page does not display for users without a walk up role

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1920787

</td><td>

Estimated waiting time displayed in the queue because related Work Items have no Assignment rule

</td></tr><tr><td>

Web UX Runtime

</td><td>

PRB1983522

</td><td>

The sn-canvas-tabs component displays a record preview popup on hover that is inaccessible to keyboard and screen reader users

</td></tr><tr><td>

Web UX Runtime

</td><td>

PRB1893204

</td><td>

Keyboard focus order on tab items and related controls is not logical for Workspace tabs

</td></tr><tr><td>

Web UX Runtime

</td><td>

PRB1920689

</td><td>

screensData contains unexpected parent data for primary tab, causing dirty screenData state

</td></tr><tr><td>

Word Document APIs

</td><td>

PRB1967960

</td><td>

Custom fonts in Word documents throw an error

</td></tr><tr><td>

Word Document APIs

</td><td>

PRB1971900

</td><td>

If a document has modified content controls with track changes turned on, document generation fails when Sync Document is performed

</td></tr><tr><td>

Workflow Editor

</td><td>

PRB1956774

</td><td>

Workflow inputs of string \(Full UTF-8\) types are missing a value

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1914183

</td><td>

Google Maps API doesn't work when calculating travel time in Field Service Management when changing the system date format

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1917452

</td><td>

Travel time and work time validation doesn't prevent the work order tasks from being updated, and the 'Close incomplete' button has unexpected results

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1931220

</td><td>

Estimated travel duration shows the incorrect message when the travel duration is valid and contains '1970-01-01'

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1934000

</td><td>

Agent Timeoff Created flow error reading, "Error: Cannot read property "start\_time" from undefined"

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1935240

</td><td>

Duplicate events appear when the schedule of a personal event changes

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1948216

</td><td>

The wm\_task\_initiator role is referenced by its sys\_id rather than by name in security attributes

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1955190

</td><td>

The 'Reschedule' UI action isn't displaying any appointments

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1960720

</td><td>

If two-step is enabled, the REQ for the part request isn't created using the CartJS.orderNow\(\) method for \_submitPartRequestOrder

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1964615

</td><td>

The Dispatcher Workspace Agents calendar shows availability on holidays

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1967578

</td><td>

The Enterprise Asset Manager role conflicts with a Field Service Management Qualifier role

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1971177

</td><td>

'Auto Assign' suggests and assigns work order tasks \(WOTs\) to agents who are already booked by other tasks, resulting in double-booking FSM

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1912592

</td><td>

There's an incorrect info message for work order tasks

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1921026

</td><td>

'Status' field choices differ from those on the 'Work Order' form view when setting up a Work Order Task \(WOT\) template

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1929488

</td><td>

The location field is not reliably set to 'Optional' due to incorrect use of getReference\(\) in client script

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1930371

</td><td>

Drag and drop blocks WOT's assignation

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1931704

</td><td>

All Work Order records are visible to users who have only the snc\_internal role

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1932040

</td><td>

Multiple errors from 'Date checks' BR on sm\_task table

</td></tr><tr><td>

Work Order Questionnaires

</td><td>

PRB1919237

</td><td>

Users are unable to view the attachment linked to a survey when retaking the survey

</td></tr><tr><td>

Work Order Questionnaires

</td><td>

PRB1936777

</td><td>

RIsk Assessment Method Statements Questionnaire of other agents can be viewed

</td></tr><tr><td>

Work Order Questionnaires

</td><td>

PRB1926607

</td><td>

string\_value missing in ast\_metric\_result records

</td></tr><tr><td>

Workspace List Menu

</td><td>

PRB1935619

</td><td>

Intermittently the L1 \(left side toolbar\) menu doesn't render in workspaces

</td></tr><tr><td>

Workspace List Menu

</td><td>

PRB1958912

</td><td>

The 'Contains' operator displays in workspaces for fields with encrypted data

</td></tr><tr><td>

Workspace List Menu

</td><td>

PRB1897679

</td><td>

In Yokohama, bookmarks on the workspace with filters are broken

</td></tr><tr><td>

Zing Text Indexing and Search Engine

</td><td>

PRB1920659

</td><td>

NoClassDefFoundError appears when initializing JapaneseTokenizer due to uninitialized TokenInfoDictionary

</td></tr><tr><td>

Zing Text Indexing and Search Engine

</td><td>

PRB1926406

</td><td>

Improve the syscache\_text\_indexable\_table\_detail caching mechanism

</td></tr><tr><td>

Zing Text Indexing and Search Engine

</td><td>

PRB1972145

</td><td>

The query is slow from the TS Index Stats job from the getTableList method

</td></tr><tr><td>

Zing Text Indexing and Search Engine

</td><td>

PRB1982399

</td><td>

Choice field is not indexed if there is no language configured for Zing

</td></tr><tr><td>

Zing Text Indexing and Search Engine

</td><td>

PRB1919510

</td><td>

Slow queries that time out go unhandled and leave the global search in an infinite loading state

</td></tr></tbody>
</table>**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


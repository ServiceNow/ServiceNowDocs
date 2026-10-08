---
title: Skill inputs for touchpoint and meeting skills
description: Table and field inputs for the touchpoint summarization, transcript analysis, prep brief, and next steps skills.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-otto-skill-inputs-touchpoints.html
release: brazil
topic_type: reference
last_updated: "2026-09-22"
reading_time_minutes: 1
keywords: [skill inputs, touchpoint, meeting]
breadcrumb: [Skill inputs, Reference, Customer Success Management]
---

# Skill inputs for touchpoint and meeting skills

Table and field inputs for the touchpoint summarization, transcript analysis, prep brief, and next steps skills.

## Touchpoint summarization skill

Includes the inputs that identify the table and fields used when a touchpoint summary is generated.

|Input|Description|
|-----|-----------|
|Input table|Touchpoint \[sn\_acct\_lc\_touchpoint\]|
|Input fields|Squad, Progress|

|Input|Description|
|-----|-----------|
|Input table|Meeting details|
|Input fields|Conference details, Meeting type, Meeting start time, Meeting end time, Customer notes, Meeting notes, State|

## Transcript Analysis skill

Analyzes a transcript chunk against the full meeting overview, next steps, and topic summaries to extract per-participant communication style, focus area, and sentiment, plus a chunk-level sentiment score.

|Input|Description|
|-----|-----------|
|Input table|Virtual Meeting Details table \(sn\_meeting\_mgmt\_virtual\_meeting\_details\)|
|Input fields|Conversation analysis, Meeting information|

## Prep Brief Data Generator skill

Produces a structured, citation-backed preparation brief for an upcoming customer meeting.

|Input|Description|
|-----|-----------|
|Input table|Virtual Meeting Details table \(sn\_meeting\_mgmt\_virtual\_meeting\_details\)|
|Input fields|Emails since last meeting, Touchpoint reference records, Stakeholders, Series classification, Meeting, Prior meetings, Account|

## Next Steps Task Description skill

Generates short and detailed task descriptions plus an assignee for each meeting. Creates next steps or actions required using the meeting overview and summary as context.

|Input|Description|
|-----|-----------|
|Input table|Meeting Details table \(sn\_meeting\_mgmt\_meeting\_details\)|
|Input fields|Meeting summary, Meeting overview|

**Parent Topic:**[Skill inputs for ServiceNow Otto for Customer Success Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-otto-skill-inputs-reference.md)


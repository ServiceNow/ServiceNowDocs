---
title: Action item collaborator synchronization with Smart Assessment
description: When users are assigned to a recovery action item, they are automatically synced as collaborators on the linked Smart Assessment instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/action-item-collaborators-smart-assessment-sync-events.html
release: zurich
topic_type: concept
last_updated: "2026-08-12"
reading_time_minutes: 1
keywords: [BCM, action item, Smart Assessment, collaborators]
breadcrumb: [Creating action items in events, Structured workflows for exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Action item collaborator synchronization with Smart Assessment

When users are assigned to a recovery action item, they are automatically synced as collaborators on the linked Smart Assessment instance.

When an action item of type Assessment transitions to **Work in progress**, a linked Smart Assessment Engine instance is created. The users assigned to the action item are synced as the assessor and collaborators on that instance.

## Assessor assignment

User in the action item's **Assigned to** field becomes the assessment assessor. If **Assigned to** is empty, the assignment group manager becomes the assessor.

This applies both when the assessment is created and after the action item is updated.

## Collaborator sync

The following users are added to assessment collaborators:

-   Users from Additional assignee list
-   Members of the assignment group
-   Assignment group manager \(unless already the assessor\)

**Note:** The current assessor is excluded from the collaborator list.

## Technical details

|Attribute|Value|
|---------|-----|
|Table|sn\_recovery\_event\_item|
|Trigger|After UPDATE|
|Filter|Type = assessment AND assessment\_template is not empty|
|Monitored Fields|assigned\_to, assignment\_group, additional\_assignee\_list|

**Parent Topic:**[Creating action items in events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/creating-action-items-in-events.md)


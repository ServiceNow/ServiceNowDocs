---
title: Action item collaborator synchronization with Smart Assessment
description: When users are assigned to a recovery action item, they are automatically synced as collaborators on the linked Smart Assessment instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/action-item-collaborators-smart-assessment-sync.html
release: australia
topic_type: concept
last_updated: "2026-07-14"
reading_time_minutes: 1
keywords: [BCM, action item, Smart Assessment, collaborators]
breadcrumb: [Creating action items in crisis events, Structured workflows for Crisis events, Manage, Business Continuity Management, Governance, Risk, and Compliance]
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

## Reverse sync: Smart Assessment to action item

When collaborators are added or removed directly on the assessment, the action item's Additional assignee list updates automatically.

## Loop protection

If an action item syncs to Smart Assessment and Smart Assessment syncs back to action item, it may repeat endlessly without loop protection. Loop protection prevents infinite back-and-forth syncing between the two records.

When assignment group members are added to the assessment, they stay as a group and not as individual names. This way, when the assessment syncs back to the action item, it doesn't trigger another sync, breaking the loop.

## Technical details

|Attribute|Value|
|---------|-----|
|Table|sn\_recovery\_event\_item|
|Trigger|After UPDATE|
|Filter|Type = assessment AND assessment\_template is not empty|
|Monitored Fields|assigned\_to, assignment\_group, additional\_assignee\_list|

**Parent Topic:**[Creating action items in crisis events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/creating-action-items-in-crisis.md)


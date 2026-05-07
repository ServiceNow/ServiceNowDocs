---
title: Define Palo Alto Networks Approval Rules
description: Activate approval workflows to require approval or rejection of EDL entries before they take effect.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Palo Alto Networks integration, Firewall integration, TISC Security Tools integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Define Palo Alto Networks Approval Rules

Activate approval workflows to require approval or rejection of EDL entries before they take effect.

## Before you begin

Role required: sn\_sec\_tisc.admin

**Important:** Save the newly configured Palo Alto Networks configuration before proceeding.

## About this task

As a TISC admin, you define these approval rules to grant consent on approval requests. You can also define multiple levels of approval.

## Procedure

1.  Navigate to the **EDL Approval Rules** section.

2.  Select **New** to create an approval rule.

    The following rules are the preconfigured rules in the base system for the Palo Alto Networks - Firewall integration.

    |Name|Description|EDL Action|
    |----|-----------|----------|
    |Approval rule for adding to EDL|Activates the approval workflow for adding entries to EDL.|Add to EDL|
    |Approval rule for removing from EDL|Activates the approval workflow for removing entries from EDL.|Remove from EDL|

3.  Fill in the form fields as appropriately.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the approval rule.|
    |EDL Action|Option to add or remove the EDL entry.|
    |EDLs|Select the EDLs that require approval. If you leave this empty, it includes all EDLs.|
    |Description|Description for the approval rule.|
    |**Select User or Groups requiring approval**|
    |User\(s\)|User\(s\) that require approval.|
    |Group\(s\)|Group\(s\) that require approval.|
    |**Select approver\(s\)**|
    |User\(s\)|User\(s\) for approval.|
    |Group\(s\)|Group\(s\) for approval.|
    |**Notifications**|
    |Notify requester on approval|When selected, notifies the requester on approval of EDLs.|
    |Notify requester on rejection|When selected, notifies the requester on rejection of EDLs.|

4.  Select **Save** to validate and save the approval rule.

5.  Select **Enable** to enable the approval rule.


**Parent Topic:**[Palo Alto Networks integration](../concept/palo-alto-networks-integration.md)

**Related topics**  


[Create EDL for Palo Alto Networks](create-new-edl.md)

[Approve EDL entries for Palo Alto Networks](tisc-approve-edl-entries.md)


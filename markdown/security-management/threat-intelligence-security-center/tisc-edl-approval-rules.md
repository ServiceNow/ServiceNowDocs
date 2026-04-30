---
title: Palo Alto EDL Approval Rules
description: Approval rules allows the users to activate the approval work flow required to approve or reject the EDL entries.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2024-10-22"
reading_time_minutes: 1
breadcrumb: [Palo Alto Networks integration, TISC Security Tools - Firewall, TISC Security Tools integrations, TISC Integrations, Integrating Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Palo Alto EDL Approval Rules

Approval rules allows the users to activate the approval work flow required to approve or reject the EDL entries.

## Before you begin

Role required: sn\_sec\_tisc.admin

## About this task

The TISC admin defines these approval rules to grant consent on the approval requests. As a TISC admin, you can also define multiple levels of approval from here.

## Procedure

1.  After you save the newly configured Palo Alto NGFW configuration, navigate to **EDL Approval Rules** section.

2.  Click **New** to create a new approval rule.

    The following rules are the pre configured rules in the base system for the Palo Alto NGFW integration.

    |Name|Description|EDL Action|
    |----|-----------|----------|
    |Approval rule for adding to EDL|This approval rule allow the users to activate the approval work flow for adding entries to EDL.|Add to EDL|
    |Approval rule for removing from EDL|This approval rule allow the users to activate the approval work flow for removing entries from EDL.|Remove from EDL|

3.  Fill the fields in the form as appropriate.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the approval rule.|
    |EDL Action|Option to add or remove the EDL entry.|
    |EDLs|Select the EDLs that requires approval. If you leave this empty then it will include all the EDLs.|
    |Description|Enter the description for the approval rule.|
    |Select User or Groups requiring approval|
    |User\(s\)|Select the user\(s\) that requires approval.|
    |Group\(s\)|Select the group\(s\) that requires approval.|
    |Select approver\(s\)|
    |User\(s\)|Select the user\(s\) for approval.|
    |Group\(s\)|Select the group\(s\) for approval.|
    |Notifications|
    |Notify requester on approval|Select this check box to notify the requester on approval of EDLs.|
    |Notify requester on rejection|Select this check box to notify the requester on rejection of EDLs.|

4.  Click **Save** to validate and save the approval rule.

5.  Click **Enable** to enable the approval rule.


**Parent Topic:**[Palo Alto Networks integration](../concept/palo-alto-networks-integration.md)


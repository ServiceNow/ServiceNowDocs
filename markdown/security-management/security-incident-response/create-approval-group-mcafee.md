---
title: Create an approval group
description: Create an approval group for the McAfee ePO for Security Operations integration that can approve requests for isolating host machines, restoring them to the network.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [McAfee ePO integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create an approval group

Create an approval group for the McAfee ePO for Security Operations integration that can approve requests for isolating host machines, restoring them to the network.

## Before you begin

You can't reassign the approval authority to a group, unless an approval group is available in your instance.

**Note:** The approvals option in the [Configure settings](../concept/mcafee-epo-configuring-profile.md) appears only for Isolate Host and Remove Host Isolation capabilities.

Role required: ServiceNow AI Platform® Security incident administrator \(sn\_si.admin\)

## About this task

Approval requests submitted by the security incident analyst to isolate host machines and remove isolation are assigned to the user with the sn\_si.admin role by default. As a user with this role, you can reassign this approval authority during the configuration step for a profile. Before you can reassign authority to an approval group, an approval group must be available on the `Groups` list in your ServiceNow AI Platform instance.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Groups**.

2.  In the groups list, click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the group that is displayed when an approval request is submitted, for example, `Approvers McAfee host isolation`.|
    |Group email|Group email distribution list or the email address of the point of contact, such as the group manager, `McAfeeapproval@servicenow`.com|
    |Manager|Name of group manager. Click the search icon to view the list.|
    |Parent|\(Optional\) Other group of which this group is a member, if this group has a parent.|
    |Description|Additional information about this group.|
    |Include members|Option to include members to this group.|
    |Default assignee|Option to choose a user as default assignee for this group. Use the Search option to open the list of users.|
    |Roles|Option to select the roles for this group. Use the Add and Remove option to add and remove roles.|
    |Type|Option to choose a category for this group. Use the Search option to open the list of group types.|
    |Vendors|Option to choose a vendor for this group. Use the Search option to open the list of vendors.|

4.  Click **Submit**.

    The new group is displayed in the Groups list.

    This group is available to process requests when you enable the **Require approval** option during the configuration of this profile.

    To monitor and process requests submitted by users with the sn\_si.analyst role, each member of the approval group navigates to **My Approvals** tab in the ServiceNow AI Platform.


**Parent Topic:**[McAfee ePO integration](../concept/mcaffee-epo-overview-arch.md)

**Previous topic:**[Edit security tags in the ServiceNow AI Platform for the McAfee ePO integration](mcafee-epo-match-tags.md)

**Next topic:**[McAfee ePO integration capability profiles](../concept/mcafee-epo-creating-profiles.md)


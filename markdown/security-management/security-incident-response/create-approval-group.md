---
title: Create an approval group
description: Create an approval group for the CrowdStrike Falcon Insight for Security Operations integration that can approve requests for isolating host machines, restoring them to the network, and initiating sightings searches.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CrowdStrike Falcon Insight integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create an approval group

Create an approval group for the CrowdStrike Falcon Insight for Security Operations integration that can approve requests for isolating host machines, restoring them to the network, and initiating sightings searches.

## Before you begin

You can't reassign the approval authority to a group, unless an approval group is available in your instance.

**Note:** The approvals option in the [profile configuration](configure-profiles-and-security-incidents-for-the-crowdstrike-falcon-insight-integration.md) appears only for Isolate Host and Remove Host Isolation capabilities.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Groups**.

2.  In the groups list, click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the group that you see when you submit an approval request.|
    |Group email|Group email distribution list or the email address of the point of contact, such as the group manager.|
    |Manager|Name of the group manager. Click the search icon to view the list.|
    |Parent|Name of the parent group, if associated with a parent.|
    |Type|Categories of groups.|
    |Vendors|vendor\_manager role that you assign to users in your organization's vendor management process.|
    |Description|Additional information about the group.|

4.  Click **Submit**.

    The new group is displayed in the Groups list.

    This group is available to process requests when you enable the **Require approval** option during the configuration of this profile.

    To monitor and process requests submitted by users with the sn\_si.analyst role, each member of the approval group navigates to **My Approvals** tab in the ServiceNow AI Platform.


## What to do next

The next step is to [install and configure](install-and-configure-crowdstrike-falcon-insight.md) the CrowdStrike Falcon Insight application from the ServiceNow Store.


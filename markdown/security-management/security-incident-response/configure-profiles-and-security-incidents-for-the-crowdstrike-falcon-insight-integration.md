---
title: Configure profiles and security incidents for the CrowdStrike Falcon Insight integration
description: Configure your profile settings so that the profile triggers only under the conditions that you set.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CrowdStrike Falcon Insight integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure profiles and security incidents for the CrowdStrike Falcon Insight integration

Configure your profile settings so that the profile triggers only under the conditions that you set.

## Before you begin

Role required: sn\_si.admin

## About this task

Define the conditions that automatically trigger the CrowdStrike Falcon Insight capabilities that you selected for the profile. You can also select an alternate input field for the Configuration Item \(CI\) field. In this alternate field, you can set filtering conditions so that only those security incidents that are related to your triggering event automatically trigger the profile.

**Note:** Navigate to the Profile Configuration page only after you enter the profile details. For more information, see [Create a capability profile for the CrowdStrike Falcon Insight integration](create-a-capability-profile-for-the-crowdstrike-falcon-insight-integration.md).

## Procedure

1.  In the Profile Configuration page, review and configure the following sections:

    **Define Incident Criteria \(Automation\)**

    Define the security incident conditions that automatically trigger the CrowdStrike Falcon Insight capabilities for the profile. If you don't select the **Define Incident Criteria** option, the capabilities are invoked manually from the security incident.

    1.  Select the **Define Incident Criteria** option.

    2.  To define the conditions, in the Filter Conditions section, select a field and its corresponding requirement.![Aautomation condition.](../image/falcon-insight-automation.png)

    3.  In the **New Criteria** field, enter the new criteria and then define the **OR** or the **AND** condition.![Automation condition and adding a new criteria.](../image/falcon-insight-automation-criteria.png)

    **Approvals**

    To provide an extra level of control when you’re using the CrowdStrike Falcon Insight capabilities, select the **Require Approval** option. The approvals option in the profile configuration appears only for the Isolate Host and Remove Host Isolation capabilities.

    **Note:** The approval authority is assigned to the user with the sn\_si.admin role. You can also reassign this approval authority to an approval group. For more information, see [set up an approval group](create-approval-group.md).

    ![Provide additional level of control using the approval option.](../image/falcon-insight-approval.png)

    **Additional Configuration**

    Select an alternate field on the security incident to display any matching CI data that you find while scanning your assets. By default, the integration uses the Configuration Item \(CI\) field on the security incident.

    1.  Select the **Define Alternative Field** option.

    2.  In the **Alternate CI Trigger Field**, select an input field.

        **Note:** For more information, see [Understand how trigger conditions work with a configuration item for a profile](../concept/define-trigger-conditions.md).

    **Tags**

    To tag security incidents with the CrowdStrike Falcon Insight Capabilities- Initiated, and Capabilities-Completed, and Capabilities-Failed tags, select the **Display Tags** option. By default, this option is disabled for all profiles.

    **Note:** These tags are provided with the base system. You can create your own tags if required.

    ![Display tags in the security incident](../image/falcon-insight-display-tags.png)

2.  Click **Done**.



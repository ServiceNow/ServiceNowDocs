---
title: Configure profiles and security incidents for the Microsoft Defender for Endpoint integration
description: Create a profile and select the Microsoft Defender for Endpoint capabilities that you want the profile to run. You need to configure the settings so that the profile can be triggered only under the defined conditions.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure profiles and security incidents for the Microsoft Defender for Endpoint integration

Create a profile and select the Microsoft Defender for Endpoint capabilities that you want the profile to run. You need to configure the settings so that the profile can be triggered only under the defined conditions.

## Before you begin

Role required: sn\_si.admin, sn\_si.analyst \(read-only\)

## About this task

Configure the profile so that it runs only when the conditions you specify are fulfilled. If required, you can select an alternate input field for the Configuration Item \(CI\) field, and set filtering conditions so that the profile can be triggered automatically when a security incident meeting the trigger conditions is created.

**Note:** You can navigate to the Profile Configuration page only after you have entered the Profile Details page.

## Procedure

1.  Navigate to **Microsoft Defender for Endpoint** &gt; **Capability Profiles**.

2.  After completing the Profile details section, click **Next**.

    Review and configure the sections.

3.  In the Define Incident Criteria \(Automation\) section, select the **Define Incident Criteria** option to automatically trigger Microsoft Defender for Endpoint capabilities in the profile.

    Define Incident Criteria \(Automation\): Define the security incident conditions that would automatically trigger the Microsoft Defender for Endpoint capabilities for the profile. If you do not select the **Define Incident Criteria** option, then the profile and the underlying capabilities can be invoked manually from the Security incident.

    **Note:** Isolate Host and Remove Host Isolation capabilities cannot be triggered automatically.

    1.  In the **Filter Conditions**, select the required field.

    2.  Add **New Criteria** and also define the **OR** or the **AND** condition.

4.  In the Approvals section, select the **Require Approval** check box to provide an extra level of control.

    If you select this option, then you have more control when using the Microsoft Defender for Endpoint capabilities for isolating host machines, restoring them to the network, getting files.

    The Approvals option in the profile configuration appears only for Isolate Host and Remove Host Isolation capabilities respectively.

5.  In the Additional Configuration section, select the **Define Alternative Field** option to define an alternative input field.

    Additional Configuration: When the Configuration item \(CI\) field is not populated on the security incident with a host name, or an IP address that matches the database, you can select an alternate field on the security incident to query the Microsoft Defender for Endpoint APIs.

    **Note:** For more information, see [Trigger conditions in a configuration item](../reference/trigger-conditions-configuration-item.md).

    1.  Select the **Define Alternative Field** option.

    2.  Select the input field from the **Alternate CI Trigger Field**.

6.  In the Tags section, select the **Display Tag** check box to enable tagging security incidents, profile name is prefixed on enabling the tag.

    You can optionally tag security incidents with tags for profile initiated, profile completed, and profile failed tags. By default, this option is turned off for all profiles.

7.  Click **Done**.



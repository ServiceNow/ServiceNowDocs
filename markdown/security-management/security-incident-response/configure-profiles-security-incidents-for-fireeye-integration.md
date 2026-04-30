---
title: Configure profiles and security incidents for the FireEye HX integration
description: After you create a profile and select the FireEye HX capabilities that you want the profile to run, configure the settings so that the profile can be invoked only under the defined conditions.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [FireEye Endpoint Security integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure profiles and security incidents for the FireEye HX integration

After you create a profile and select the FireEye HX capabilities that you want the profile to run, configure the settings so that the profile can be invoked only under the defined conditions.

## Before you begin

Role required: sn\_si.admin

Configure the profile so that it runs only when the conditions you specify are fulfilled. Select an alternate input field for the Configuration Item \(CI\) field, if required, and set filtering conditions so that the profile can be triggered automatically when a security incident meeting the trigger conditions is created.

**Note:** You can navigate to the **Profile Configuration** page only after you have entered the **Profile Details**.

## Procedure

1.  Navigate to **FireEye Integration** &gt; **FireEye Capability Profiles**.

2.  Click **Next** on the **Profile Details** page after completing the Profile details section.

3.  Review and configure the following sections:

    -   **Define Incident Criteria \(Automation\)**: Define the security incident conditions that would automatically trigger the FireEye HX capabilities for the profile. If you do not select the **Define Incident Criteria** option, then the profile and the underlying capabilities can be invoked manually from the Security incident.
        -   Select **Define Incident Criteria** option to automatically trigger FireEye HX capabilities in the profile.
        -   In the **Filter Conditions**, select the required field.
        -   You can add **New Criteria** and also define the OR or the AND condition.

            **Note:** Isolate Host, Remove Host Isolation, Get File cannot be triggered automatically.

    -   **Additional Configuration**: When the Configuration item \(CI\) field is not populated on the security incident with a host name, or an IP address that matches the database, you can select an alternate field on the security incident to query the FireEye HX APIs.

        -   Select the **Define Alternative Field** option to define an alternative input field.
        -   Select the input field from the **Alternate CI Trigger Field**.

            **Note:** For more information, see [Understand how trigger conditions work with a configuration item](../concept/understand-trigger-conditions-work-with-configuration-item.md).

        ![Additional Configuration section for FireEye Capability Profile.](../image/additional-config.png)

    -   **Tags**: You can optionally tag security incidents with the FireEye HX profile initiated, profile completed, and profile failed tags.

        Select the **Display Tag** check box to enable tagging security incidents, profile name is prefixed on enabling the tag. By default, this option is disabled for all profiles.

        ![Enabling Tags for security incidents.](../image/display-tag.png)

    -   **Approvals**: Select the **Require Approval** check box to provide an extra level of control when using the FireEye HX capabilities for isolating host machines, restoring them to the network, and to get the files.

        The approvals option in the profile configuration appears only for Isolate Host, Remove Host Isolation, and Get File capabilities.

        ![Setting up parameters in the Approval section.](../image/approval-checkbox.png)

4.  Click **Done**.

5.  Verify FireEye HX trigger conditions.



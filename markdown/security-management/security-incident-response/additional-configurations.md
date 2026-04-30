---
title: FireEye Default Settings
description: Following are the additional configuration settings after you complete the installation.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Install the application and configure a source for the integration, FireEye Endpoint Security integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# FireEye Default Settings

Following are the additional configuration settings after you complete the installation.

Once you complete the installation, you can find FireEye Default Settings module in the left navigation. It contains default settings for different FireEye functionalities.

## Additional Configurations

Following are the additional configuration settings:

1.  **Approval**: This approval is specifically for the Isolate Host, Remove Host Isolation, and Get File capabilities when they are triggered directly from the Related list, and in the absence of profiles for them. If there is/\(are\) \(an\) existing profile\(s\) for these capabilities, then the approval configuration in the profile will be honored.
    -   **Require Approval:** When you enable Require Approval, the Approvers field is available on the form.
    -   **Approvers**: List of approver groups. After you submit a request, approval is required from the group to complete the request.
2.  **Alternate CI**: Enabling this check box will provide list of fields available to pass an alternate CI to the capability. By default, the integration uses the Configuration Item \(CI\) field on the Security incident. This configuration is applicable only for the “Run Additional Actions on Endpoint” capability. So, use this configuration to define an alternate CI input field for the “Run Additional Actions on Endpoint” capability only. For the other capabilities use the configuration in the profile section. If the profiles do not define an alternate CI, then the capabilities would pick the CI field from the Security Incident form.
3.  **Input for Agent ID resolution**: By default, IP and Host Name will be used to get the Agent ID. If only one of them is to be used set the input field to either IP or Host Name.

    ![FireEye Default Settings](../image/fireeye-additional-settings.png)

4.  **Timeout**:

    -   **Base Capabilities Timeout\(minutes\):** The Enrichment, Isolate Host and Remove Host Isolation capabilities will fail if no response is rendered in the set time.
    -   **Additional Action Timeout\(minutes\):** The Run Additional Actions on End point capability will fail if no response is rendered in the set time.
    -   **File Acquisition Timeout\(minutes\):** The Get File capability will fail if no response is rendered in the set time.
    -   **Sighting Search Timeout\(minutes\):** The Search will be stopped after the set time.
    ![FireEye Default Settings extended page](../image/fireeye-additional-settings01.png)



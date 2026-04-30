---
title: Microsoft Defender for Endpoint Default Settings
description: There are additional configuration settings you must perform after you complete the installation.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Install and configure, Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Microsoft Defender for Endpoint Default Settings

There are additional configuration settings you must perform after you complete the installation.

After you complete the installation, you can find the Default Settings module under the Microsoft Defender for Endpoint application on the left-navigation pane. It contains the default settings for different Microsoft Defender for Endpoint functionalities.

Roles required: sn\_si.admin, sn\_si.analyst \(read-only\).

## Additional Configurations

The following are additional configuration settings:

-   **Approval**: This approval is specifically for the Isolate Host action, Remove Host Isolation action, and additional actions such as Restrict App Execution, Remove App Restriction and Run Antivirus Scan. You can use this approval only when actions are triggered directly from the Related list, and if there are no any existing profiles. If there are any existing profiles for these capabilities, then the approval configuration in the profile takes precedence.
    -   **Require Approval**: When you enable **Require Approval**, the Approvers field is available on the form.
    -   **Approvers**: List of approver groups. After you submit a request, approval is required from the group to complete the request.
-   **Alternate CI**: Enabling this check box provides the list of fields available to pass an alternate CI to the capability. By default, the integration uses the Configuration Item \(CI\) field on the Security incident. This configuration is applicable only for the Run Additional Actions on Endpoint capability. Use this configuration to define an alternate CI input field for the only Run Additional Actions on Endpoint capability. For the other capabilities, use the configuration in the profile section. If the profiles do not define an alternate CI, then the capabilities would take the CI field from the Security Incident form.
-   **Input for Agent ID resolution**: By default, IP and Host Name is used to get the Agent ID. If you're going to use only one of them, then set the input field to either IP or Host Name.
-   **Timeout**:
    -   **Isolate Host Timeout \(in minutes\):** Indicates the execution threshold for the Isolate Host capabilities.
    -   **Remove Isolation Timeout \(in minutes\):** Indicates the execution threshold for the Remove Isolation Timeout capability.
    -   **Restrict App Execution Timeout \(in minutes\):** Indicates the execution threshold for the Restrict App Execution capability.
    -   **Remove App Restriction Timeout \(in minutes\):** Indicates the execution threshold for the Remove App Restriction capability.
    -   **Run Antivirus Scan Timeout \(in minutes\):** Indicates the execution threshold for the Run Antivirus Scan capability.
    -   **Stop and Quarantine File Timeout \(in minutes\):** Indicates the execution threshold for the Stop and Quarantine File capability.

![Additional configuration settings after you complete the installation](../image/ms_defender_default_settings.png "Default Settings")


---
title: Walk-up Experience Badge Reader Integration setup and configuration
description: Badge Reader Integration set up and configuration enables your on-site Walk-up Experience users to scan a badge to quickly check into the queue.
locale: en-US
release: australia
product: Walk-Up Experience
classification: walk-up-experience
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Badge Reader Integration for Walk-up Experience, Configure, Walk-up Experience, IT Service Management]
---

# Walk-up Experience Badge Reader Integration setup and configuration

Badge Reader Integration set up and configuration enables your on-site Walk-up Experience users to scan a badge to quickly check into the queue.

The Walk-up Experience \(com.snc.walkup\) and Badge Reader Integration \(com.snc.badge\_reader\) plugins must be activated before you set up and configure the integration. Refer to [Activate Walk-up Experience](../task/activate-walkup-experience.md) and [Activate Badge Reader Integration](../task/activate-badge-reader-integration.md) for details regarding activation.

Badge Reader Integration is automatically activated with Walk-up Experience via a conditional plugin.

Set up and configuration entails the following stages:

-   Client software: Create your own custom badge reader client software to integrate with the badge reader.
-   Badge reader device: Configure the badge reader device and register it manually or via an assisted process.
-   Approval: Request and receiving device activation approval.
-   Walk-up Experience application: Configure Walk-up Experience to integrate with a badge reader device.

-   **[Create or modify Badge Reader Integration event handlers](../task/create-or-modify-badge-event-handlers.md)**  
Configure actions associated with a badge scan event and define the code to execute when a badge is scanned.
-   **[Define and register a badge reader device using the badge reader client](../task/assisted-config-badge-read-settings.md)**  
Use the Badge Reader Client to create a badge reader device for registration in your system. Registering your badge reader enables you to make it operational at your Walk-up Experience on-site queue.
-   **[Define and register a badge reader device manually](../task/config-badge-reader-settings.md)**  
Manually create a badge reader device for registration in your system. Registering your badge reader enables you to make it operational at your Walk-up Experience on-site queue.
-   **[Define a user badge configuration](../task/define-user-badge-configuration.md)**  
Define the table from where the user ID and Badge ID mapping information is retrieved.
-   **[Request activation approval for a badge reader device](../task/request-badge-reader-device-approval.md)**  
Request activation approval for your badge reader device. Badge Reader Integration will not trigger event handlers until the badge reader is activated. Badge reader device approval and activation is granted by users with the itil role.
-   **[Configure Walk-up Experience for Badge Reader Integration](../task/config-walkup-for-badge-read-integ.md)**  
Associate badge reader devices with an on-site Walk-up Experience queue. While you can associate more than one badge reader device to a walk-up location, individual badge reader devices are mapped to only one walk-up location.
-   **[Customize badge Reader Integration](badge-reader-integ-customization.md)**  
Badge Reader Integration includes several scripted extension points for you to customize script includes installed with the feature.

**Parent Topic:**[Badge Reader Integration for Walk-up Experience](badge-scan-walkup-onsite.md)


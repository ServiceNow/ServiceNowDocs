---
title: Configuring Digital End-User Experience
description: You can set up and configure Digital End-User Experience based on your organization's specific requirements. Learn how to integrate web and installed applications and to manage the Application and Device Health monitoring system.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Digital End-User Experience, IT Service Management]
---

# Configuring Digital End-User Experience

You can set up and configure Digital End-User Experience based on your organization's specific requirements. Learn how to integrate web and installed applications and to manage the Application and Device Health monitoring system.

Before setting up and using Digital End-User Experience \(DEX\), confirm that the system meets the minimum requirements to guarantee optimal performance. For more information, see [DEX system requirements](dex-sys-requirements.md).

To set up DEX and begin exploring the workspace, you must complete the following configurations.

1.  [Install Application and Device Health.](../task/install-app-device-health.md)
2.  Install Agent Client Collector \(ACC\).
    -   [Create an ACC registration key](../task/setup-acc.md).
    -   [Test connectivity to the ServiceNow instance](../task/test-connectivity-to-instance.md)
    -   [Install ACC for DEX on Windows](../task/install-acc-for-dex-windows.md)
    -   [Install ACC for DEX on macOS](../task/install-acc-for-dex-macos.md)
    -   [Test Agent Client Collector connectivity](../task/test-acc-connectivity.md)
    -   If you have a MID-based ACC, you must convert it to a MID-less ACC. For more information regarding conversion, see [Convert MID-based ACC to MID-less](../task/convert-midbased-acc.md).
    -   If you want to fetch the complete playbook content data for a Windows device, see [Run ACC as a local system account user](../task/run-acc-local-sys-account.md).
3.  [Enable DEX browser extension](../task/enable-dex-browser-extension.md).
4.  [Onboard for Application and Device Health.](../task/dex-onboarding.md)
5.  Make sure to [Configure MID-less Agent Client Collector using a single-line command](../../../reuse/agent-client-collector-and-dex/configure-acc-midless.md).
6.  [Explore Application &amp; Device Health interface](accessing-pages.md).

    **Note:** DEX Content Playbook provides policies, check definitions, and actions that can be used by Application and Device Health to facilitate the monitoring of applications and devices, and to support application remediation. You can also refer to [DEX Content Playbook reference](../reference/dex-content-playbook-reference.md) to learn the content it provides.

7.  [Set up DEX Desktop Assistant](config-dex-desktop-exp.md).
8.  [Configure Proactive Engagement](../../proactive-engagement/configuring-proactive-engagement.md).
9.  [Configure DEX Self-service.](configuring-dex-self-service.md)
10. [Configure Digital Experience Score​](../../dex-score/concept/dexscr-configuring-dex-score.md).


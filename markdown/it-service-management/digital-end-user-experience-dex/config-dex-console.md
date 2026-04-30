---
title: Configuring Digital End-User Experience
description: Set up and configure Digital End-User Experience. Learn how to integrate web/SaaS or installed applications and to make modifications or removals from the Application and Device Health monitoring system. Customize the Desktop Assistant by organizing the Home page into sections and adding cards to these sections, enhancing your efficiency and accessibility.
locale: en-US
release: xanadu
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Digital End-User Experience, IT Service Management]
---

# Configuring Digital End-User Experience

Set up and configure Digital End-User Experience. Learn how to integrate web/SaaS or installed applications and to make modifications or removals from the Application and Device Health monitoring system. Customize the Desktop Assistant by organizing the Home page into sections and adding cards to these sections, enhancing your efficiency and accessibility.

Before setting up and using Digital End-User Experience \(DEX\), confirm that the system meets the minimum requirements to guarantee optimal performance. For more information, see [DEX system requirements](dex-sys-requirements.md).

To set up DEX and begin exploring the workspace, you must complete the following configurations.

1.  [Install Application and Device Health.](../task/install-app-device-health.md)
2.  [Create an ACC registration key](../task/setup-acc.md).
3.  [Install ACC for DEX on Windows](../task/install-acc-for-dex-windows.md) or [Install ACC for DEX on macOS](../task/install-acc-for-dex-macos.md).
    -   If you want to install Agent Client Collector \(ACC\) on Windows and Mac manually, see [Install the Agent Client Collector on a Windows machine manually](https://www.servicenow.com/docs/access?context=acc-install-windows&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) or [Manually install Agent Client Collector on macOS](https://www.servicenow.com/docs/access?context=acc-install-macOS-manual&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US). Verify you [configure MID-less ACC](../task/config-midless-acc.md) before proceeding to the next configuration step.
    -   If you have a MID-based ACC, you must convert it to a MID-less ACC. For more information regarding conversion, see [Convert MID-based ACC to MID-less](../task/convert-midbased-acc.md).
    -   If you want to fetch the complete playbook content data for a Windows device, see [Run ACC as a local system account user](../task/run-acc-local-sys-account.md).
4.  [Enable DEX browser extension](../task/enable-dex-browser-extension.md).
5.  [Onboard for Application and Device Health.](../task/dex-onboarding.md)
6.  [Explore Application &amp; Device Health interface](accessing-pages.md).

    **Note:** DEX Content Playbook provides policies, check definitions, and actions that can be used by Application and Device Health to facilitate the monitoring of applications and devices, and to support application remediation. You can also refer to [DEX Content Playbook reference](../reference/dex-content-playbook-reference.md) to learn the content it provides.

7.  [Setting up DEX Desktop Assistant](config-dex-desktop-exp.md).


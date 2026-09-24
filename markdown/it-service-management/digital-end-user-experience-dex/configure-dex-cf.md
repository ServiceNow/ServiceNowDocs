---
title: Configuring Digital End-User Experience
description: As a DEX administrator, install and configure Digital End-User Experience to monitor end-user applications, devices, and networks. Complete the core setup for Application and Device Health, and then configure the optional components and integrations that match the DEX capabilities your organization has licensed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/configure-dex-cf.html
release: brazil
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [configure, set up, install, digital end-user experience, dex, agent client collector, acc, application monitoring, device monitoring, network monitoring, browser extension, metric rules, event rules, alerts, agent policy, remedial actions, non-persistent vdi, microsoft 365, zoom, dex score, proactive engagement, self-service, guided setup, desktop assistant]
audience: administrator
breadcrumb: [Digital End-User Experience, IT Service Management]
---

# Configuring Digital End-User Experience

As a DEX administrator, install and configure Digital End-User Experience to monitor end-user applications, devices, and networks. Complete the core setup for Application and Device Health, and then configure the optional components and integrations that match the DEX capabilities your organization has licensed.

## Configuration overview

Complete the core setup steps in the order listed to get DEX operational for basic application and device monitoring.

1.  [Before you begin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/dex-before-you-begin.md)

    Review the subscription options and confirm that your instance meets the DEX system requirements before installing.

2.  [Installing DEX on your local machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/installing-dex-local.md)

    Install Application and Device Health and set up the Agent Client Collector \(ACC\) on Windows and macOS end-user devices. Test connectivity and enable the DEX browser extension for web application monitoring.

3.  [Deploying DEX to employees](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/deploying-dex-to-employees.md)

    Distribute Agent Client Collector and the browser extension to your employees' devices at scale.

4.  [DEX application monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/dex-application-monitoring.md)

    Onboard applications, add applications to monitor, and enable or disable monitoring per application.

5.  [Managing DEX alert rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/dex-metrics-metric-rules-management.md)

    Create metric rules and event rules to detect issues in the metrics that DEX collects.

6.  [DEX Alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/dex-alerts.md)

    Configure how DEX raises alerts, creates incidents from alerts, and groups related alerts.


After the core setup is in place, use the checklist that follows to configure the optional DEX capabilities and integrations that apply to your deployment. Not every organization needs every capability.

|Configuration area|Description|
|------------------|-----------|
|[Collecting DEX metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/managing-metrics-collection.md)|Change how often DEX collects metrics and adjust which metrics are collected.|
|[Create an agent policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/create-agent-policy.md)|Create agent policies that control Agent Client Collector behavior on the devices you monitor.|
|[Creating DEX remedial actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/dex-remedial-actions.md)|Create and package remedial actions, check definitions, and playbooks so that DEX can resolve detected issues automatically or with agent approval.|
|[Event monitoring with DEX](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/event-monitoring-dex.md)|Add events for DEX to monitor on end-user devices.|
|[Non-persistent VDI monitoring configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/monitoring-np-vdis.md)|Install and configure Agent Client Collector on non-persistent virtual desktop infrastructure \(VDI\) golden images.|
|[Setting up DEX insights and lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/dex-insights-and-lists.md)|Set up Windows registry key collection, file management data collection, and compliance reporting.|
|[Configuring DEX for Microsoft 365](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/configuring-dex-for-microsoft-365.md)|Register a custom application in the Microsoft Azure portal and set up OAuth to monitor Microsoft 365 and Teams call quality.|
|[Configuring DEX for Zoom](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/configuring-DEX-for-Zoom.md)|Create a connected Zoom app and add a Zoom connection to monitor Zoom call quality and Zoom Rooms.|
|[Advanced configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/dex-advanced-configuration.md)|Configure Agent Client Collector proxy settings, MID Server-less operation, sudo banner handling, device-user mapping, and location determination.|
|[Setting up DEX Desktop Assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/config-dex-desktop-exp.md)|Download, configure, and customize Desktop Assistant for Windows and macOS, including theming, notifications, Virtual Agent chat, and Employee Center home page cards.|
|[Setting up Proactive Engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/setting-up-proactive-engagement.md)|Install and configure Proactive Engagement to detect issues and trigger self-solve engagements for employees.|
|[Configuring Digital End-user Experience Self-service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/configuring-dex-self-service.md)|Enable Digital End-user Experience Self-service and configure the issues, categories, and device actions that employees can access from Employee Center, Desktop Assistant, and Virtual Agent.|
|[Configuring Digital Experience Score​](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/dexscr-configuring-dex-score.md)|Configure the Digital Experience Score​ dashboard, including metric definitions, quality-to-score mapping, and survey configuration.|

## Using guided setup to implement Digital End-User Experience

Guided setup provides a sequence of tasks that help you install and configure DEX and its associated plugins on your ServiceNow instance. Guided setup covers agent deployment on Windows and macOS devices, browser extension deployment, Desktop Assistant deployment, and Digital End-user Experience Self-service configuration.

To open guided setup, in the primary navigation pane, select the DEX Administration icon \(\[Omitted image "icon-administration.png"\] Alt text:\).

For more information, see [DEX guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/dex-install-config.md).


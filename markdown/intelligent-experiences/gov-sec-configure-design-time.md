---
title: Activate design-time security metrics
description: Set up AI Service Graph Connectors for the AI security tools you currently use to import AI model vulnerability and AI validation \(automated red teaming\) data and show it in design-time metrics. To see additional metrics, including details for each metric, install the AI Security Exposure Management plugin \(com.sn\_sec\_ai\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-sec-configure-design-time.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Managing AI asset security, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Activate design-time security metrics

Set up AI Service Graph Connectors for the AI security tools you currently use to import AI model vulnerability and AI validation \(automated red teaming\) data and show it in design-time metrics. To see additional metrics, including details for each metric, install the AI Security Exposure Management plugin \(com.sn\_sec\_ai\).

## Before you begin

Role required: admin

Review [the application listing](https://store.servicenow.com/store/app/a36ed8ba873f7e94a6c6fc48cebb358f) in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

## About this task

AI Service Graph Connectors are available for third-party AI security tools \(for example, Cisco AI Defense or HiddenLayer\). Install and configure the Service Graph Connector for the security tool you use to see the data reflected in design-time metrics.

The AI Security Exposure Management plugin \(`com.sn_sec_ai`\) provides these additional metrics: Findings approaching remediation target, Findings with remediation overdue, Findings deferred, and Posture findings by risk rating on the AI security posture sub-tab;Approaching remediation target, Remediation overdue, Vulnerabilities deferred, and Vulnerabilities by risk on the AI vulnerabilities sub-tab; and Approaching remediation target, Remediation overdue, and Findings deferred on the AI validation sub-tab. It also provides drilldown details for every design-time metric.

If the AI Security Exposure Management plugin isn't installed, a source dropdown appears at the top of the Design-time tab, letting you filter the AI security posture, AI vulnerabilities, and AI validation sub-tab metrics by source.

## Procedure

1.  Install the AI Service Graph Connector for each third-party AI security tool for which you want data reflected in design-time metrics.

    For more information, see [Getting started with Service Graph Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/cmdb-sgc-intro.md).

    Next, you can optionally install the AI Security Exposure Management plugin to get additional metric details and more.

2.  With the link provided, open the ServiceNow Store listing for the [AI Security Exposure Management plugin](https://store.servicenow.com/store/app/ee19aa89472d03582339f6cc416d432b) \(com.sn\_sec\_ai\).

3.  Select **Get**.

4.  After approval has been granted, on your instance, navigate to **Admin****Application Manager**

5.  Search for the AI Security Exposure Management plugin \(com.sn\_sec\_ai\).

6.  Select **Install**.


**Parent Topic:**[Configuring security metrics in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-configuring.md)


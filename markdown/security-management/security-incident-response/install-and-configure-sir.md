---
title: Install and configure Security Incident Response
description: Before you run Security Incident Response in your instance, you must download it from the ServiceNow Store and complete configuration steps.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Security Incident Response setup, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Install and configure Security Incident Response

Before you run Security Incident Response in your instance, you must download it from the ServiceNow Store and complete configuration steps.

## Before you begin

Role required: admin

**Important:**

-   Installing the Security Incident Response 13.4.5 version or later from the ServiceNow Store will automatically install the Security Incident Response Workspace \(sn\_si\_aw\) 1.5.1 version or later by default. For more information on the dependent applications, refer to the [SIR Workspace plugins](../../secops-analyst-workspace/reference/components-installed-with-analyst-workspace.md) section.
-   Please note that the Security Incident Response Workspace versions 1.5.1 and above can only be installed/upgraded through an installation/upgradation of Security Incident Response and cannot be installed independently.
-   The latest features in Security Incident Response are exclusively available in the Security Incident Response Workspace. Please install or upgrade to the latest Security Incident Response or Security Incident Response Workspace version to access and leverage features such as Shift-Handover, Risk Score Calculator, etc.

## Procedure

1.  Follow the instructions for [downloading an application from the ServiceNow Store](../reference/download-app-first-time.md).

2.  After you have downloaded the Security Incident Response application and all of its dependency applications, navigate to **Security Incident** &gt; **Analyst Workspace Setup** &gt; **Setup Assistant**.

    ![Security Incident Response setup assistant](../image/sir-setup-assistant.png)

3.  Follow the instructions on the forms to configure the Security Incident Response base system.

    For additional information on some of the more complicated setup tasks, see [Setup Assistant reference](../reference/setup-assistant-reference.md#), as needed.



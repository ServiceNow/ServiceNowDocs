---
title: Configure Microsoft Defender for Office 365 integration
description: Gain valuable insights into phishing simulation metrics directly within the Cybersecurity Executive Dashboard through seamless integration with Microsoft Defender for Office 365.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [what are requirements for integration, how to configure microsoft defender for office 365 integration, how to set up phishing simulation]
breadcrumb: [Security Simulation and Training Integration for Security Operations, Cybersecurity Executive Dashboard, Security Operations]
---

# Configure Microsoft Defender for Office 365 integration

Gain valuable insights into phishing simulation metrics directly within the Cybersecurity Executive Dashboard through seamless integration with Microsoft Defender for Office 365.

## Before you begin

Role required: sn\_sec\_phish\_msatk.ms\_admin

## About this task

To learn more about simulating a phishing attack and setting up a tenant, see:

-   [Simulate a phishing attack with Attack simulation training](https://learn.microsoft.com/en-us/defender-office-365/attack-simulation-training-simulations)
-   [Getting started using Attack simulation training](https://learn.microsoft.com/en-us/defender-office-365/attack-simulation-training-get-started)
-   [Set up a tenant](https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-create-new-tenant)

## Procedure

1.  Navigate to **All** &gt; **Microsoft Attack Integration** &gt; **Microsoft Attack Configurations**.

2.  Select **New**.

3.  On the form, fill in the details:

    |Field|Description|
    |-----|-----------|
    |Integration Instance|Name of the integration instance. Select the integration instance using the Lookup icon.|
    |Tenant ID|Tenant ID of the application created on the Microsoft Azure portal.|
    |Client ID|Client ID of the application created on the Microsoft Azure portal.|
    |Client Secret|Client secret of the application created on the Microsoft Azure portal.|
    |Bookmark|Date from which the simulations must be fetched.|
    |Token Url|Base URL from where the token is created to access the Microsoft Simulations API.|
    |All Simulation Url|Base URL of the Microsoft Simulations API.|

    1.  Select **New** if no integration instance is available.

    2.  On the form, fill in the details:

        |Field|Description|
        |-----|-----------|
        |Name|Name of the integration instance.|
        |Application|Name of the application \(Microsoft Defender for Office 365\).|
        |Integration|Third-party integration reference \(Microsoft Attack Integration\).|
        |Active|Default is activated \(selected\). If cleared, the instance isn't active.|
        |Description|Short description of the integration instance.|

4.  Select **Submit**.

5.  Navigate to **All** &gt; **Security Simulation and Training** &gt; **Integrations**.

6.  Select Microsoft Attack integration.

7.  Select **Execute Now** to execute and collect data from Microsoft.



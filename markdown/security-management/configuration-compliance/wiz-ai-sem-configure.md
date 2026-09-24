---
title: Configure Wiz AI Security Exposure Management routing
description: Configure the Wiz integration to send posture findings for AI resources to AI Security Exposure Management instead of Configuration Compliance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/configuration-compliance/wiz-ai-sem-configure.html
release: brazil
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Wiz, AI Security Exposure Management, posture findings, integration]
breadcrumb: [Integrate, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Configure Wiz AI Security Exposure Management routing

Configure the Wiz integration to send posture findings for AI resources to AI Security Exposure Management instead of Configuration Compliance.

## Before you begin

Before you begin, verify the following:

-   The AI Security \(sn\_sec\_ai\) plugin is active. The routing option is hidden on the configuration form until this plugin is active.
-   The Vulnerability Response Integration with Wiz application is installed and an existing Wiz integration is configured.

Role required: sn\_vul\_wiz.configure\_integration

## About this task

Users with the sn\_vul\_wiz.read\_integration role can view whether this option is enabled without being able to change it.

## Procedure

1.  Navigate to **All** &gt; **Wiz Vulnerability Integration** &gt; **Administration** &gt; **Configuration**.

2.  Select the **Test Results Configuration** tab.

3.  Select the **Insert AI records into AI Security Exposure Management** check box.

    **Note:** This feature is only visible if you have installed [AI Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/exploring-ai-security-exposure.md).

    Imports cloud configuration findings as Test Results into Configuration Compliance. Configuration issues related to AI assets, such as AI models and agents are routed into AI security exposure management tables \(AI posture findings\) if this feature is activated.

4.  Select **Save**.


## Result

After you save the configuration with this option selected, it cannot be turned off. A field message on the form states this before you save. This restriction is enforced by a before-update business rule and applies even if a change is attempted through an API or import, not only through the form.

Configuration Compliance stops creating test results for the posture findings that are routed to AI Security. This avoids the same finding appearing twice, once as a Configuration Compliance test result and once as an AI Security finding. Any Configuration Compliance test results already created for AI resources before you enabled this option are not removed. Only new findings are affected.


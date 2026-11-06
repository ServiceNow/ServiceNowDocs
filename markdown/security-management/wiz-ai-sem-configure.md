---
title: Configure the Wiz AI Security Exposure Management integration
description: Configure the integration to send a sub-set of cloud configuration findings relevant to AI security to the AI posture findings table in AI Security Exposure Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/security-management/wiz-ai-sem-configure.html
release: australia
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 3
keywords: [Wiz, AI Security Exposure Management, posture findings, integration]
breadcrumb: [Wiz AI Security Exposure Management integration, Integrate, Unified Security Exposure Management, Security Operations]
---

# Configure the Wiz AI Security Exposure Management integration

Configure the integration to send a sub-set of cloud configuration findings relevant to AI security to the AI posture findings table in AI Security Exposure Management.

## Before you begin

As described in the [Wiz AI Security Exposure Management integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/wiz-ai-sem-integration.md) overview, there are two types of findings that can be imported from Wiz

-   Cloud configuration findings related to AI security.
-   AI security findings \(model, agent, MCP risk\).

For the AI security findings \(model, agent, MCP risk\), it is not required to enable any specific configuration. These findings are imported by default when Wiz integration credentials are provided and submitted. However, note that Unified Security Exposure Management \(USEM\) must already be installed on your instance to import these findings and the service account configured for the Wiz integration must have the permission: read:ai\_security\_findings.

For the cloud configuration findings related to AI security, you must first enable a setting that is described in the following steps on the **Test Results Configuration** tab for the Wiz Test Results Integration. The Wiz Test Results Integration is included with the Vulnerability Response Integration with Wiz.

Verify the following applications are installed and activated:

-   Unified Security Exposure Management \(USEM\) is installed on your instance.
-   The AI Security \(sn\_sec\_ai\) plugin is active. The routing option described in the following steps is hidden on the configuration form until activate this plugin.
-   The Vulnerability Response Integration with Wiz application is installed and activated. See [Activate the Vulnerability Response Integration with Wiz application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/vulnerability-response/vr-wiz-host-vuln-install.md) and [Configure the Wiz AI Security Exposure Management integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/wiz-ai-sem-configure.md).

Role required: sn\_vul\_wiz.configure\_integration

## About this task

**Note:** With the sn\_vul\_wiz.read\_integration role, you can view the **Send AI security findings to AI security exposure management** check box option but can't change it.

## Procedure

1.  Navigate to **All** &gt; **Wiz Vulnerability Integration** &gt; **Administration** &gt; **Configuration**.

2.  Select the **Test Results Configuration** tab.

3.  Select the **Send AI security findings to AI security exposure management** check box.

    **Note:** This feature is only visible if you have installed [AI Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/exploring-ai-security-exposure.md).

    Sends posture findings for AI resources to AI Security Exposure Management rather than creating them as test results in Configuration Compliance.

    **Note:** If you don't enable this option and you're Importing cloud configuration findings described in [Wiz AI Security Exposure Management integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/wiz-ai-sem-integration.md), these findings are imported as Test Results into Configuration Compliance.

4.  Select **Save**.


## Result

After you save the configuration with this option selected, it cannot be turned off. A field message on the form states this before you save. This restriction is enforced by a before-update business rule and applies even if a change is attempted through an API or import, not only through the form.

Configuration Compliance stops creating test results for the posture findings that are routed to AI Security. This avoids the same finding appearing twice, once as a Configuration Compliance test result and once as an AI Security finding. Any Configuration Compliance test results already created for AI resources before you enable this option are not removed. Only new findings are affected.


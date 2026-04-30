---
title: Get started with the CrowdStrike Falcon X Sandbox integration
description: Activate and set up the CrowdStrike Falcon X Sandbox to interface with your ServiceNow instance and Security Incident Response product.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [CrowdStrike Falcon X Sandbox integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Get started with the CrowdStrike Falcon X Sandbox integration

Activate and set up the CrowdStrike Falcon X Sandbox to interface with your ServiceNow instance and Security Incident Response product.

## Before you begin

-   Before you can use the CrowdStrike Falcon X Sandbox for Security Operations integration, you must download it from the [ServiceNow Store](../../../planning-and-policy/concept/secops-and-store.md).
-   Review the following setup checklist and verify that you have completed all the tasks for a smooth CrowdStrike Falcon X Sandbox integration.

Role required: admin, sn\_si.admin

<table id="table_yvc_gb3_1nb"><thead><tr><th>

Setup task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify that you have assigned the required ServiceNow AI Platform and Security Incident Response roles.

</td><td>

The following roles are required for configuration and verification of the expected results:-   The administrator \(admin\) installs the sandbox integration from the ServiceNow app store and assigns the security incident administrator \(sn\_si.admin\) role.
-   The sn\_si.admin creates and edits the configuration and global settings and then assigns the security incident analyst \(sn\_si.analyst\) role.
-   The security incident analyst \(sn\_si.analyst\) responds to security incidents, such as submitting files and URLs to the sandbox and analyzing the submission results.

</td></tr><tr><td>

Verify that the ServiceNow core applications that are required to support the integration are installed and activated before you configure this integration.

</td><td>

This integration is supported on Paris and Orlando releases.

 Ensure that these dependent plugins are installed. These plugins enable the execution of Integration Hub actions and flows:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)

**Note:** If you can't find a plugin, you may have to request it from ServiceNow personnel. To request a plugin, follow the steps in [Request a plugin](https://www.servicenow.com/docs/access?context=t_RequestAPlugin&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

 The Security Incident Response plugin \(com.snc.security\_incident\) is required. This plugin automatically installs all the dependencies that are required to support the Security Incident Response product. Install and activate this plugin before you install and activate the other Security Operations applications that are required by the integration.

 Verify that the following Security Operations applications are installed and activated from the ServiceNow Store. If not installed, install and activate one application at a time in the following order to ensure a smooth installation.

 1.  Security Incident Response Dependency \(com.snc.si\_dep\)
2.  Security Integration Framework
3.  Security Support Common
4.  Security Support Orchestration
5.  Threat Intelligence Support Common \(required to use the sandbox integration capabilities\)
6.  Trusted Security Circles
7.  Security Operations Setup Assistant
8.  Security Incident Response

 For more information on setting up your ServiceNow AI Platform instance for the integration, see [Get entitlement for a Security Operations product](../../../security-incident-response/task/entitle-secops-product.md) or application and [Activate a ServiceNow Store application](../../../security-incident-response/task/activate-entitled-store-app.md).

</td></tr><tr><td>

Verify that you are licensed for the Falcon Sandbox Private API key, and obtain the CrowdStrike Falcon X Sandbox full API key.

</td><td>

This integration supports the Falcon Sandbox Private Cloud only.

**Note:** This release does not support Falcon X integration.

 CrowdStrike Falcon X Sandbox offers a self-signed restricted API key and an upgraded full API key. Use the full API key for this integration because it enables unrestricted access for automated submissions.

 For more information, see [CrowdStrike Falcon Sandbox Knowledge Base](https://www.falcon-sandbox.com/knowledge-base/issuing-full-api-key-for-automated-submissions).

</td></tr></tbody>
</table>## Procedure

1.  [Download the CrowdStrike Falcon Sandbox for Security Operations integration from the ServiceNow Store](../../../security-incident-response/reference/download-app-first-time.md).

2.  When the installation is complete, navigate to Security Operations &gt; Integrations &gt; Integration Configurations.

3.  Search for the CrowdStrike Falcon X Sandbox integration tile, and click **Configure**.

4.  Enter the following details to complete the configuration:

    |Field|Description|
    |-----|-----------|
    |**Name**|Name of this integration, for example, `demo-1`. While this is a unique name to identify the sandbox configuration, you can only configure one integration per ServiceNow instance.|
    |**CrowdStrike Falcon Sandbox Base URL**|Sandbox base URL. This URL is available after you configure the sandbox.For example, `https://servicenow.falcon-sandbox.com` is a base URL.|
    |**Client ID**|OAuth2 API client ID. For more information see, [API Clients and Keys](https://falcon.crowdstrike.com/login/?next=%2Fsupport%2Fapi-clients-and-keys).|
    |**Client Secret**|OAuth2 API client secret key. For more information see, [API Clients and Keys](https://falcon.crowdstrike.com/login/?next=%2Fsupport%2Fapi-clients-and-keys).|

5.  Click **Submit**.

    After the sandbox is successfully validated and submitted, it is saved on the Security Integrations page as a tile. You can now view the Sandbox module in the application navigator.

    ![Sandbox links in the application navigator.](../image/sandbox-links.png)


## What to do next

After you successfully complete the integration, the next step is to set up [Sandbox submission configurations](setup-sandbox-submission-configurations.md).


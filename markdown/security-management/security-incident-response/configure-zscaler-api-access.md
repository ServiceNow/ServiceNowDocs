---
title: Configure access to Zscaler Internet Access APIs
description: Configure access to the Zscaler Internet Access server to authenticate the secure connection between the ServiceNow AI Platform instance and the Zscaler server.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Security Incident Response integration with Zscaler, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure access to Zscaler Internet Access APIs

Configure access to the Zscaler Internet Access server to authenticate the secure connection between the ServiceNow AI Platform instance and the Zscaler server.

## Before you begin

Role required: Zscaler Internet Access admin

ServiceNow supports the following API role configurations for the Zscaler integration.

-   **Service Admin Role**:

    Create the API key using a role with Service Admin privileges.

    This configuration provides full functionality and is recommended for environments without strict role-segregation requirements.

-   **Least-Privilege Role \(Supported\)**:

    For users who require reduced privilege, ServiceNow supports a least-privilege configuration.

    Create a custom role with the following permissions:

    -   **Security: Custom**
    -   **Malware Protection, Sandbox, &amp; Advanced Threat Protection: Full**
    When configured with these permissions, the integration runs as expected.


## About this task

After Zscaler enables your API subscription for your organization's cloud service, it is available in the Zscaler Internet Access API key management page with the base URL. Your organization can only have one API key or token. Delete the existing key or token before you add a new one.

The base URL for the API is `${Cloud_Name}/api/v1`. Check the Zscaler cloud name that was provisioned for your organization and use it to replace `{Cloud_Name}` in the base URI. Some examples of the base URL are:

-   example.zscalerbeta.net
-   example.zscalerone.net
-   example.zscalertwo.net
-   example.zscaler.net
-   example.zscloud.net

**Note:** For more information about the Zscaler Internet Access administration portal, see the [Zscaler API key management documentation](https://help.zscaler.com/zia/about-api-key-management) and the [Zscaler Portal documentation](https://help.zscaler.com/cloud-connector/about-cloud-connector-portal).

## Procedure

1.  Log in as an admin to the Zscaler Internet Access administration portal.

2.  Navigate to **Administration** &gt; **Cloud Service API Security**.

3.  Select **Add API Key**.

    If you do not see the **Add API Key** option, delete the existing key.

    The new API key is immediately valid and is displayed in the tab.


## Result

You have retrieved the base URL and the API key to configure access to Zscaler from the ServiceNow AI Platform instance.


---
title: Discover firewall policies
description: As a member of a security team, you can discover firewall devices, policies, and owner groups, allowing a central view of the footprint. This data is updated in the ServiceNow CMDB. Set up a schedule to discover your firewall policies to help you keep track of your company's valuable information.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Visibility to Firewall inventory, Configuring Firewall Audits and Reporting, Firewall Audits and Reporting, ITOM Visibility, IT Operations Management]
---

# Discover firewall policies

As a member of a security team, you can discover firewall devices, policies, and owner groups, allowing a central view of the footprint. This data is updated in the ServiceNow CMDB. Set up a schedule to discover your firewall policies to help you keep track of your company's valuable information.

## Before you begin

For the Panorama integration, you must have a Superuser \(Read only\) role.

Role required: discovery\_admin or admin

## About this task

Administrators in charge of Discovery can establish a recurring schedule for Palo Alto Networks firewall policy discovery. This schedule utilizes the serverless pattern, connecting with the Palo Alto Firewall Manager to discover and update information for the following four Configuration Items \(CIs\) in the CMDB.

-   Panorama Firewall Manager \[cmdb\_ci\_firewall\_manager\_panorama\]
-   Palo Alto Firewall Devices \[cmdb\_ci\_firewall\_device\_palo\_alto\]
-   Panorama Firewall Device Group \[cmdb\_ci\_firewall\_device\_group\_panorama\]
-   Panorama Firewall Security Policies \[cmdb\_ci\_firewall\_sec\_policy\_panorama\]

## Procedure

1.  Create a new credential alias of type **API Key Credentials** and **Submit** the credential.

2.  Enter the Panorama API key.

    For more information, see [Credential aliases for Discovery](https://www.servicenow.com/docs/access?context=discovery-credential-alias&version=australia&pubname=australia-platform-security&ft:locale=en-US).

3.  To create a Discovery schedule, perform the following steps.

    1.  Select **Discover: Serverless**.
    2.  Select the appropriate **MID Server**.
    3.  Right-click the header and select **Save**.
    For more information on Discovery schedule, see [Schedule a horizontal discovery](t_CreateADiscoverySchedule.md#).

4.  From the tab at the bottom of the screen, select the Serverless Execution pattern and then select **New**.

5.  In the Serverless Execution pattern, perform the following steps.

    1.  Enter a name.
    2.  Select **PaloAlto - Firewall Manager**.
    3.  Select **Run Child Patterns**.
    4.  Select **Submit**.
6.  Navigate to **Discovery Pattern Launcher Parameters** and set the following three parameters.

    -   credentialAlias: Provide the new credential alias name created in step 1.
    -   trustInsecureHosts: Set to **true** to turn off hostname verification and enable self-signed certificates to be accepted as trusted.
    -   url: Enter the base URL of the Panorama device.

        For example, https:// &lt;PANORAMA\_HOST&gt;/api.

7.  Right-click the header and select **Save**.


**Parent Topic:**[Visibility to Firewall inventory](../concept/use-firewall-audit-rep.md)


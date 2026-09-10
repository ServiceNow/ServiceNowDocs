---
title: Discover firewall policies
description: As a member of a security team, you can discover firewall devices, policies, and owner groups from supported vendors \(Palo Alto Panorama and Fortinet FortiManager\), allowing a central view of the footprint. This data is updated in the ServiceNow CMDB. Set up a schedule to discover your firewall policies to help you keep track of your company's valuable information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/discovery/disco-firewall-policies.html
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Visibility to Firewall inventory, Configuring Firewall Audits and Reporting, Firewall Audits and Reporting, Discovery, ITOM Visibility, IT Operations Management]
---

# Discover firewall policies

As a member of a security team, you can discover firewall devices, policies, and owner groups from supported vendors \(Palo Alto Panorama and Fortinet FortiManager\), allowing a central view of the footprint. This data is updated in the ServiceNow CMDB. Set up a schedule to discover your firewall policies to help you keep track of your company's valuable information.

## Before you begin

Role required: discovery\_admin, firewall\_admin

## About this task

Administrators in charge of Discovery can establish a recurring schedule for firewall policy discovery. This schedule utilizes the serverless pattern, connecting with the firewall manager to discover and update information for Configuration Items \(CIs\) in the CMDB.

For Fortinet FortiManager-specific requirements, including MID Server sizing and API endpoint information, see .

<table id="table_firewall_cis"><thead><tr><th>

Vendor

</th><th>

CMDB Configuration Items

</th><th>

Non-CMDB Tables

</th></tr></thead><tbody><tr><td>

Palo Alto Panorama

</td><td>

-   Panorama Firewall Manager \[cmdb\_ci\_firewall\_manager\_panorama\]
-   Palo Alto Firewall Devices \[cmdb\_ci\_firewall\_device\_palo\_alto\]
-   Panorama Firewall Device Group \[cmdb\_ci\_firewall\_device\_group\_panorama\]
-   Panorama Firewall Security Policies \[cmdb\_ci\_firewall\_sec\_policy\_panorama\]

</td><td>

-   Panorama Address Objects
-   Panorama Address Group Objects
-   Panorama Service Objects
-   Panorama Service Group Objects
-   Policy Object M2M References

</td></tr><tr><td>

Fortinet FortiManager

</td><td>

-   FortiManager Network Manager \[cmdb\_ci\_fortimanager\_network\_manager\]
-   Fortinet Firewall ADOM \[cmdb\_ci\_firewall\_device\_group\_fortinet\]
-   Fortinet Firewall Device \[cmdb\_ci\_firewall\_device\_fortinet\]
-   Fortinet Firewall Policy Package \[cmdb\_ci\_fortinet\_firewall\_policy\_pkg\]
-   Fortinet Firewall Policy \[cmdb\_ci\_fortinet\_firewall\_policy\]

</td><td>

-   Fortinet Address Objects \[sn\_disco\_firewall\_fortinet\_address\_object\]
-   Fortinet Address Group Objects \[sn\_disco\_firewall\_fortinet\_addrgrp\_object\]
-   Fortinet Service Objects \[sn\_disco\_firewall\_fortinet\_service\_object\]
-   Fortinet Service Group Objects \[sn\_disco\_firewall\_fortinet\_servicegrp\_object\]
-   Fortinet VIP Objects \[sn\_disco\_firewall\_fortinet\_vip\_object\]
-   Fortinet VIP Group Objects \[sn\_disco\_firewall\_fortinet\_vipgrp\_object\]
-   Fortinet ISDB Objects \[sn\_disco\_firewall\_fortinet\_isdb\_object\]
-   Firewall Policy Object M2M Mappings \[sn\_disco\_firewall\_policy\_object\_m2m\]

</td></tr></tbody>
</table>## Procedure

1.  Create a new credential of type **API Key Credentials**.

    Enter the API key for your firewall vendor in the credential record.

2.  Create a credential alias for the API key credential created in the previous step.

    You provide this credential alias in the discovery schedule configuration. For more information, see [Credential aliases for Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/discovery-credential-alias.md).

3.  To create a Discovery schedule, perform the following steps.

    1.  Select **Discover: Serverless**.
    2.  Select the appropriate **MID Server**.
    3.  Right-click the header and select **Save**.
    For more information on Discovery schedule, see [Schedule a horizontal discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/t_CreateADiscoverySchedule.md).

4.  From the tab at the bottom of the screen, select the Serverless Execution pattern and then select **New**.

5.  In the Serverless Execution pattern, perform the following steps.

    1.  Enter a name.
    2.  Select the pattern for your vendor:
        -   For Palo Alto Panorama: Select **PaloAlto - Firewall Manager**.
        -   For Fortinet FortiManager: Select **Fortinet FortiManager \(LP\)**.
    3.  Select **Run Child Patterns**.
    4.  Select **Submit**.
6.  Navigate to **Discovery Pattern Launcher Parameters** and set the following parameters.

    -   credentialAlias: Provide the credential alias name created in step 2.
    -   For Palo Alto Panorama:
        -   url: Set to the base URL of your Panorama device \(https://&lt;PANORAMA\_HOST&gt;/api\).
        -   trustInsecureHosts: Set to **true** to turn off hostname verification and enable self-signed certificates to be accepted as trusted.
    -   For Fortinet FortiManager: Set the ipAddress parameter to the IP address of your FortiManager appliance.
7.  Right-click the header and select **Save**.


**Parent Topic:**[Visibility to Firewall inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/use-firewall-audit-rep.md)


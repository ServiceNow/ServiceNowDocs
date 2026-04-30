---
title: Set up the Check Point NGTP integration
description: Complete the following steps to set up the Check Point Next Generation Threat Prevention integration. This would ensure that the pre-requisites for the integration to work are in place.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Check Point Next Generation Threat Prevention integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up the Check Point NGTP integration

Complete the following steps to set up the Check Point Next Generation Threat Prevention integration. This would ensure that the pre-requisites for the integration to work are in place.

## Before you begin

Role required: admin

## Procedure

1.  Verify that Threat Prevention Policy is configured with Anti-Bot and Anti-Virus Blades activated.

    Refer the Check Point User Guide mentioned in Reference section for detailed information on setting up Anti-Bot and Anti-Virus Blades.

    **Note:** The images in this topic are privileged and proprietary and are used with permission from Check Point Software Technologies, Ltd.

    1.  Login to **Smart Console**.

    2.  Navigate to **Security Policies** &gt; **Threat Prevention** &gt; **Policy**.

        ![Policy](../image/policy.png)

    3.  Open the Threat Prevention Policy in Edit Mode.

        ![Edit Policy](../image/edit-policy.png)

    4.  Active Protections → Severity should be “Medium or above”

    5.  Activation Mode → High Confidence should be “Prevent”

    6.  Blades Activation à Anti-Virus and Anti-Bot should be selected.

        ![Policies optimized](../image/policies-optimized.png)

    7.  Publish the changes \(if any\) and Install the Policy.

2.  If not already configured, Custom Intelligence Feeds should be added after activating Anti-Bot and Anti-Virus Blades.

    Refer to the Installation section of Check Point Custom Intelligence Feed Feature documentation. [https://supportcenter.checkpoint.com/supportcenter/portal?eventSubmit\_doGoviewsolutiondetails=&amp;solutionid=sk132193](https://supportcenter.checkpoint.com/supportcenter/portal?eventSubmit_doGoviewsolutiondetails=&solutionid=sk132193)

3.  If not already configured, set up the Check Point Gateway to route all the internet traffic via HTTP Proxy \(if configuring HTTPS Inspection\).

    **Note:** For URL blocking on Check Point NGTP, there are certain settings that needs to be ensured. HTTPS internet traffic uses the SSL \(Secure Sockets Layer\) protocol and is encrypted to give data privacy. However, HTTPS can hide malicious traffic which should have been blocked. For Check Point Gateway to get the visibility into HTTPS traffic, either route the traffic via HTTP Proxy or setup HTTPS Inspection\(recommended\). This section details the steps to follow to setup HTTP Proxy on Check Point Gateway.

    1.  Login to **Smart Console**.

    2.  Navigate to **Servers and Gateways**, and double-click on the applicable server.

        ![Servers and gateways](../image/servers-and-gateways.png)

    3.  Navigate to **Network Management** &gt; **Proxy**.

        ![Network Management proxy](../image/network-mgmt-proxy.png)

    4.  Provide the Proxy Details to be used for routing the HTTP traffic.

    5.  Ensure that HTTP requests from Client Endpoint are via the HTTP Proxy.

4.  If not already configured, enable HTTPS inspection \(if HTTP Proxy configured\).

    When most of the traffic is over SSL, it is recommended to use HTTPS Inspection Blade. This makes the traffic transparent to GW. Enable HTTPS Inspection on Check Point Gateway, as follows.

    1.  Login to **Smart Console**.

    2.  Navigate to **Servers and Gateways**, and double-click on the applicable server.

    3.  Navigate to **HTTPS Inspection**.

        ![HTTPS inspection](../image/https-nspection.png)

    4.  Follow the [steps to configure HTTPS Inspection](https://sc1.checkpoint.com/documents/R80.10/WebAdminGuides/EN/CP_R80.10_NexGenSecurityGateway_Guide/html_frameset.htm?topic=documents/R80.10/WebAdminGuides/EN/CP_R80.10_NexGenSecurityGateway_Guide/13700) in the Check Point User Guide.



---
title: Getting started with Security Incident Response integration with Zscaler
description: Activate and set up the Zscaler Internet Access product to interface with your ServiceNow AI Platform instance and Security Incident Response product.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Security Incident Response integration with Zscaler, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Getting started with Security Incident Response integration with Zscaler

Activate and set up the Zscaler Internet Access product to interface with your ServiceNow AI Platform instance and Security Incident Response product.

<table id="table_z2c_gyj_vpb"><thead><tr><th>

Setup task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assign and verify the required ServiceNow AI Platform and Security Incident Response roles.

</td><td>

These roles are required for configuration and verification of the expected results:-   The admin role installs the integration from the ServiceNow Store and assigns the sn\_si.admin role.
-   The sn\_si.admin role performs the following tasks:
    -   Configures the integration.
    -   Creates, activates, and removes the URL Category lists.
    -   Assigns the sn\_si.analyst role.
-   The sn\_si.analyst role creates entries and works with security incidents.

</td></tr><tr><td>

Verify that the ServiceNow core applications are installed and activated before you configure this integration.

</td><td>

The ServiceNow Integration Hub Enterprise Pack Installer \[com.glide.hub.integrations.enterprise\] plugin is required.

 The Security Incident Response plugin \(com.snc.security\_incident\) is required. This plugin automatically installs all the dependencies for the Security Incident Response product. Install and activate this plugin before you install and activate the other Security Operations applications for the integration.

 Verify that the following Security Operations applications are installed and activated from the ServiceNow Store. If these applications are not already installed, install and activate each application one at a time in the following order:

 1.  Security Incident Response Dependency \(com.snc.si\_dep\)
2.  Security Integration Framework
3.  Security Support Common
4.  Security Support Orchestration
5.  Threat Intelligence Support Common
6.  Trusted Security Circles
7.  Security Operations Setup Assistant
8.  Security Incident Response

</td></tr><tr><td>

Verify the Zscaler versions.

</td><td>

-   This integration is supported on Zscaler Internet Access version 1.0 or later.
-   This integration is tested with the following Zscaler versions:
    -   Zscaler Client Connector for Windows - 3.0
    -   Zscaler Client Connector for macOS - 3.0
    -   Zscaler Client Connector for Linux - Beta
    -   Zscaler Cloud Connector - 6.1

</td></tr><tr><td>

Verify that you have the required Zscaler permissions and have configured [access to the Zscaler Internet Access APIs](../task/configure-zscaler-api-access.md).

</td><td>

-   You must have the admin credentials for Zscaler Internet Access.
-   You must have a valid cloud service API subscription. Zscaler Support must provide your key.
-   You must have Zscaler Internet Access admin credentials \(user name and password\). API authentication is based on a combination of the API key and Zscaler Internet Access admin credentials.

 **Note:** For more information on managing the Zscaler Internet Access API keys, see the [Zscaler documentation](https://help.zscaler.com/zia/api-getting-started#CreateSession).

</td></tr></tbody>
</table>
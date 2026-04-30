---
title: Getting started with the CrowdStrike Falcon Insight integration
description: You can activate and set up the CrowdStrike Falcon Insight to interface with your ServiceNow AI Platform instance and Security Incident Response product.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [CrowdStrike Falcon Insight for Security Operations integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Getting started with the CrowdStrike Falcon Insight integration

You can activate and set up the CrowdStrike Falcon Insight to interface with your ServiceNow AI Platform instance and Security Incident Response product.

## Before you begin

Role required: admin

Before you can use CrowdStrike Falcon Insight for the Security Operations integration, you must download it from the ServiceNow Store.

## About this task

<table id="table_btf_hzs_cwb"><thead><tr><th>

Setup task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assign and verify the required ServiceNow AI Platform and Security Incident Response roles.

</td><td>

These roles are required for configuration and verification of the expected results:-   The admin role installs the integration from the ServiceNow Store and assigns the sn\_si.admin role.
-   The sn\_si.admin role configures the integration, creates and activates profiles, and then assigns the sn\_si.analyst role.
-   The sn\_si.analyst role responds to security incidents, launches profiles manually, and can submit requests for such actions as isolating the host and removing the host isolation for an approved group.

</td></tr><tr><td>

Verify that the ServiceNow core applications that are required to support the integration are installed and activated before you configure this integration.

</td><td>

The ServiceNow Integration Hub Enterprise Pack Installer \[com.glide.hub.integrations.enterprise\] plugin is required. This plugin enables the execution of IntegrationHub actions and flows:

 The Security Incident Response plugin \(com.snc.security\_incident\) is required. This plugin automatically installs all the dependencies that are required to support the Security Incident Response product. Install and activate this plugin before you install and activate the other Security Operations applications that are required by the integration.

 Verify that the following Security Operations applications are installed and activated from the ServiceNow Store. If these applications are not already installed, you must install and activate each application one at a time in the following order to ensure a smooth installation:

 1.  Security Incident Response Dependency \(com.snc.si\_dep\)
2.  Security Integration Framework
3.  Security Support Common
4.  Security Support Orchestration
5.  Threat Intelligence Support Common
6.  Trusted Security Circles
7.  Security Operations Setup Assistant
8.  Security Incident Response

</td></tr><tr><td>

[Set up an approval group.](create-approval-group.md)

</td><td>

An optional approval capability is available for isolating host machines, restoring them to the network, and initiating sightings searches.

 To enable this option, you require prior approval from the sn\_si.admin role before host machines are isolated and restored to your network, or when sightings searches are performed. If you require an extra level of control over these actions, enable the **Require approval** option when configuring the profile. The approval authority is assigned to the user with the sn\_si.admin role. You can also reassign this approval authority to an approval group.

</td></tr><tr><td>

Assign and verify the CrowdStrike Falcon Platform roles.

</td><td>

The following roles are required on the CrowdStrike Falcon Platform for the integration configuration:-   The Falcon administrator role is required to view, create, or modify API clients or keys.
-   The Real Time Responder – Administrator role is required for creating and executing custom scripts.
-   The Real Time Responder – Active Responder role is required for creating and executing custom scripts.

</td></tr><tr><td>

Verify that the custom scripts roles and permissions are enabled in the CrowdStrike Falcon Platform.

</td><td>

This integration uses CrowdStrike's custom scripts for few of the enrichment capabilities. -   Verify that the Real Time Responder – Administrator and the Real Time Responder – Active Responder roles are available.
-   Verify that the **Default\(Windows\) policy** option is enabled in Configuration &gt; Response Policies in the CrowdStrike Falcon UI.
-   Verify that the **Real Time Response** and **Custom Scripts** under Real Time Functionality is enabled in the CrowdStrike Falcon UI.

</td></tr><tr><td>

[Generate API clients and keys in the CrowdStrike Falcon Platform.](create-api-clients-and-keys.md)

</td><td>

Create the CrowdStrike API clients or keys in the CrowdStrike Falcon Platform to use in the ServiceNow AI Platform integration configuration.

</td></tr></tbody>
</table>
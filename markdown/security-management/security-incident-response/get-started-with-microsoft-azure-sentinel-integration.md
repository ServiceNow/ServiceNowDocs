---
title: Get started with Microsoft Azure Sentinel integration
description: Activate and set up the Microsoft Azure Sentinel - Incident Ingestion for Security Operation plug-in to interface with your ServiceNow AI Platform instance and Security Incident Response product.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Microsoft Azure Sentinel integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Get started with Microsoft Azure Sentinel integration

Activate and set up the Microsoft Azure Sentinel - Incident Ingestion for Security Operation plug-in to interface with your ServiceNow AI Platform instance and Security Incident Response product.

**Important:**

Microsoft has extended the deprecation of the Azure Sentinel experience in the Azure portal from March 2026 to March 2027.

If you are currently using the Azure Sentinel integration with Security Incident Response \(SIR\), we strongly recommend migrating to the new Defender portal integration \(store link of the defender integration\) as soon as possible. The Defender integration includes a built-in migration utility that automatically converts your existing Sentinel profiles into Defender profiles, while ensuring continuity of incidents created through Sentinel after the transition. For more information, see XX.

Before you can use the Microsoft Azure Sentinel integration, you must download it from the ServiceNow Store.

Role required: Microsoft Azure application developer, Microsoft Azure tenant administrator.

Review the following setup checklist and verify that you’ve completed all the tasks for a smooth integration.

<table id="table_yvc_gb3_1nb"><thead><tr><th>

Setup task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assign and verify the required ServiceNow AI Platform and Security Incident Response roles.

</td><td>

The following roles are required for configuration and verification of the expected results:-   The admin role installs the integration from the ServiceNow Store and assigns the sn\_si.ingestion\_profile\_admin role.
-   The sn\_si.ingestion\_profile\_admin role performs the following tasks:
    -   Configures the integration.
    -   Creates incident profiles.
    -   Maps the Microsoft Azure Sentinel incident data fields to the security incident fields.
    -   Schedules on-going incident ingestion.
    -   Enables incident updates when a Security Incident Response incident is created or closed.
    -   Assigns the security incident analyst \(sn\_si.analyst\) role.

</td></tr><tr><td>

Assign the Microsoft Azure required roles.

</td><td>

The following roles are required in Microsoft Azure to register and configure your application:-   Application developer for registering the application.
-   Tenant administrator for giving permissions to the application by calling the admin consent endpoint.

</td></tr><tr><td>

Verify that the ServiceNow core applications that are required to support the integration are installed and activated before you configure this integration.

</td><td>

The ServiceNow Integration Hub Starter Pack Installer \[com.glide.hub.integrations\] plugin is required.

 The Security Incident Response plugin \(com.snc.security\_incident\) is required. This plugin automatically installs all the dependencies that are required to support the Security Incident Response product. Install and activate this plugin before you install and activate the other Security Operations applications that are required by the integration.

 Verify that the following Security Operations applications are installed and activated from the ServiceNow Store. If these applications aren’t already installed, you must install, and activate each application one at a time in the following order to ensure a smooth installation:

 1.  Security Incident Response
2.  Security Incident Response UI
3.  ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
4.  ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)

</td></tr><tr><td>

[Register and configure your application in the Microsoft Azure portal.](../task/configure-microsoft-azure-portal.md)

</td><td>

Register your application in the Microsoft Azure portal and grant your users with read and write access to the application.

</td></tr></tbody>
</table>
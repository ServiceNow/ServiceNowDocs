---
title: Get started with CrowdStrike Next-Gen SIEM integration
description: Activate and set up the CrowdStrike Next-Gen SIEM integration for Security Operation plug-in to interface with your ServiceNow AI Platform instance and Security Incident Response product.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-06"
reading_time_minutes: 1
breadcrumb: [CrowdStrike Next-Gen SIEM integration for Security Operations, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Get started with CrowdStrike Next-Gen SIEM integration

Activate and set up the CrowdStrike Next-Gen SIEM integration for Security Operation plug-in to interface with your ServiceNow AI Platform instance and Security Incident Response product.

Before you can use the CrowdStrike Next-Gen SIEM integration, you must download it from the ServiceNow Store.

Review the following setup checklist and verify that you’ve completed all the tasks for a smooth integration.

<table id="table_yvc_gb3_1nb"><thead><tr><th>

Setup task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assign and verify the required ServiceNow AI Platform and Security Incident Response roles.

</td><td>

The following roles are required for configuration and verification of the expected results:-   The admin role installs the integration from the ServiceNow Store and assigns the sn\_si.ingestion\_profile\_admin and sn\_si.analyst roles.
-   The sn\_si.ingestion\_profile\_admin role performs the following tasks:
    -   Configures the integration.
    -   Creates detection profiles.
    -   Maps the CrowdStrike Next-Gen SIEM detection data fields to the security incident fields.
    -   Schedules on-going detection ingestion.
    -   Enables detection updates when a Security Incident Response detection is created or closed.

</td></tr><tr><td>

Assign the CrowdStrike required roles.

</td><td>

The following roles are required in CrowdStrike to register and configure your application:-   Application developer for registering the application.
-   Tenant administrator for giving permissions to the application by calling the admin consent endpoint.

</td></tr><tr><td>

Verify that the ServiceNow core applications that are required to support the integration are installed and activated before you configure this integration.

</td><td>

The Security Incident Response plugin \(com.snc.security\_incident\) is required. This plugin automatically installs all the dependencies that are required to support the Security Incident Response product. Install and activate this plugin before you install and activate the other Security Operations applications that are required by the integration.

</td></tr><tr><td>

[Install and configure CrowdStrike Next-Gen SIEM integration](../task/cs-ng-siem-integration.md)

</td><td>

Install and configure the CrowdStrike Next-Gen SIEM integration for Security Operations application from the ServiceNow Store on your ServiceNow AI Platform instance.

</td></tr></tbody>
</table>
---
title: Get started with the Microsoft Defender for Endpoint integration
description: The following section lists the setup tasks that you are required to complete in your ServiceNow AI Platform instance prior to installing the Microsoft Defender for Endpoint application from the ServiceNow store.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Get started with the Microsoft Defender for Endpoint integration

The following section lists the setup tasks that you are required to complete in your ServiceNow AI Platform® instance prior to installing the Microsoft Defender for Endpoint application from the ServiceNow store.

## Before you begin

Role required: admin

Refer to the following table and verify that you have completed all the listed tasks before you download and install the application to ensure a smooth installation and configuration.

<table id="table_mfd_jmb_3sb"><thead><tr><th>

Setup task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify that you have assigned the required ServiceNow AI Platform and Security Incident Response \(SIR\) roles.

</td><td>

The following roles are required:1.  You must have system administrator \(admin\) role to install the application for the integration.
2.  You must have security incident administrator \(sn\_si.admin\) role to configure the integration, create, activate, and remove profiles.
3.  You must have security incident analyst \(sn\_si.analyst\) role to work with security incidents. A user with this role can initiate any of the capabilities available in the integration.

</td></tr><tr><td>

Verify that the ServiceNow core applications that are required to support the integration are installed and activated before you install the application.

</td><td>

Verify that the following Security Operations applications are installed and activated from the ServiceNow Store. If these applications are not already installed, you must install and activate each application one at a time in the following order to ensure a smooth installation:

1.  Security Incident Response
2.  ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
3.  ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)

</td></tr><tr><td>

Before you enable the approval option for profiles, verify that you have created an approval group.

</td><td>

An optional approval workflow is available for isolating host machines, restoring them back to the network, and running additional actions on end point.If your organization wants an extra level of control over these actions, enable the Require approval option during the configuration of the profiles.

 In a scenario where the profile is available, the profile configuration for approval takes precedence. In a scenario where the profile is unavailable, the approvals are handled based on the default settings.

 As a Security Administrator, you can set up approval while configuring the profiles and the default settings. An approval group must be available on the Groups list in your instance.

 To monitor and process requests submitted by the users with sn\_si.analyst role, each member of the approval group should navigate to My Approvals in the ServiceNow AI Platform®. Alternatively, the approvers can find the requests submitted exclusively for Microsoft Defender for Endpoint integration under the Approvals module. For more information on how to create a user group, see [Create a user group](https://www.servicenow.com/docs/access?context=t_CreateAGroup&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>## What to do next

You have successfully set up your ServiceNow AI Platform® instance for the Microsoft Defender for Endpoint integration. The next step is to install the Microsoft Defender for Endpoint application from the ServiceNow Store for the integration.


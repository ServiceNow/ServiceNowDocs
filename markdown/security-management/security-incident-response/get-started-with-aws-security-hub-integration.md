---
title: Get started with AWS Security Hub integration
description: Activate and set up the AWS Security Hub findings integration for Security Operation plug-in to interface with your ServiceNow instance and Security Incident Response product.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Amazon Web Services \(AWS\) Security Hub integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Get started with AWS Security Hub integration

Activate and set up the AWS Security Hub findings integration for Security Operation plug-in to interface with your ServiceNow® instance and Security Incident Response product.

## Before you begin

Role required: sn\_si.admin

Before you can use the AWS Security Hub integration, you must download it from the ServiceNow Store.

## About this task

Review the following setup checklist and verify that you’ve completed all the tasks for a smooth integration.

<table id="table_tgh_fd1_fdc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Assign and verify the required ServiceNow® platform and Security Incident Response roles.

</td><td>

The following roles are required for configuration and verification of the expected results:-   The admin role installs the integration from the ServiceNow Store and assigns the sn\_si.admin role.
-   The sn\_si.admin role performs the following tasks:
    -   Configures the integration.
    -   Creates incident profiles.
    -   Maps the AWS Security Hub finding data fields to the security incident fields.
    -   Schedules on-going incident ingestion.
    -   Enables incident updates when a Security Incident Response incident is created or closed.

</td></tr><tr><td>

Assign the AWS Security Hub required roles.

</td><td>

The following roles are required in AWS Security Hub to register and configure your application:-   SecurityHubReadOnlyAccess
-   SecurityHubFullAccess

</td></tr><tr><td>

Review the AWS Security Hub integration settings

</td><td>

Navigate to **All** &gt; **AWS Security Hub findings integration** &gt; **AWS Security Hub Findings Integration Settings**.Review or modify the properties settings according to your requirement.

</td></tr><tr><td>

Configure your application in the AWS portal.

</td><td>

Register your application in the AWS portal and grant your users with read and write access to the application.Refer to the following topics for more information:

-   [Setting Up AWS Config with the Console](https://docs.aws.amazon.com/config/latest/developerguide/gs-console.html)
-   [Security Hub integrations.](https://docs.aws.amazon.com/config/latest/developerguide/1-click-setup.html)

</td></tr></tbody>
</table>
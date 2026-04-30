---
title: Getting started with MISP integration for Security Operations
description: Review the following information before you set up your MISP integration for Security Operations.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [MISP administration, MISP integration for Security Operations, Threat Intelligence integrations, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Getting started with MISP integration for Security Operations

Review the following information before you set up your MISP integration for Security Operations.

<table id="table_k2d_1bk_ynb"><thead><tr><th>

Setup task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify that you have assigned the required ServiceNow AI Platform, Threat Intelligence, and Security Incident Response roles.

</td><td>

The following roles are used across the MISP features on the ServiceNow AI Platform:-   The administrator \(admin\) installs the applications from the ServiceNow Store and assigns the security incident administrator \(sn\_si.admin\) and threat intelligence administrator \(sn\_ti.admin\) roles.
-   sn\_si.admin and sn\_ti.admin can configure the integration and set up the automatic MISP event creation profiles.
-   sn\_sec\_misp.write - The MISP analyst role has read and write permissions for MISP data that includes the event and attribute data.

 For more information, see [Setup Threat Intelligence](../../threat-intelligence/concept/c_GetStartedWithThreatIntel.md#).

</td></tr><tr><td>

Assign the required MISP user roles.

</td><td>

[Review the MISP user roles and the permissions required to use the MISP integration for Security Operations](misp-user-roles-and-permissions.md).**Note:** For more information about the user roles in MISP, see the Roles section in the [MISP documentation website](https://www.circl.lu/doc/misp/administration/#roles).

</td></tr><tr><td>

Verify that you are using MISP version 2.4.137 or later.

</td><td>

The MISP integration for Security Operations is tested with a minimum [MISP version 2.4.137](https://www.misp-project.org/2021/01/20/MISP.2.4.137.released.html).

</td></tr><tr><td>

Verify that the ServiceNow core applications that are required to support the MISP module are installed and activated.

</td><td>

Verify that the following Security Operations applications are installed and activated from the ServiceNow Store. If not installed, install and activate one application at a time in the following order to ensure a smooth installation.

-   Security Incident Response
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)

 For more information on setting up your ServiceNow AI Platform instance for the integration, see [get entitlement for a Security Operations product](../../security-incident-response/task/entitle-secops-product.md) or application and [activate a ServiceNow Store application](../../security-incident-response/task/activate-entitled-store-app.md).

</td></tr><tr><td>

Domain separation

</td><td>

Verify the [domain separation section](domain-separation-and-misp.md) if you intend to separate data, processes, and administrative tasks.

</td></tr></tbody>
</table>-   **[MISP user roles and permissions](misp-user-roles-and-permissions.md)**  
Review the user roles that are required in the MISP integration for Security Operations integration.

**Parent Topic:**[MISP administration](../concept/misp-administration.md)

**Related topics**  


[Install and configure the MISP integration for Security Operations](../task/install-and-configure-misp.md)

[Review the MISP integration settings](../task/review-the-misp-integration-settings.md)

[Configure MISP sighting searches](../task/configure-sightings-search.md)

[Configure how an automatic event is created](../task/configure-automatic-event-creation-profile.md#)

[MISP event data](../concept/misp-event-data.md)

[Associated MISP events](associated-misp-events.md)

[MISP user information](misp-user-information.md)

[Domain separation and MISP](domain-separation-and-misp.md)

[Troubleshooting MISP integration](troubleshooting-misp-integration.md)


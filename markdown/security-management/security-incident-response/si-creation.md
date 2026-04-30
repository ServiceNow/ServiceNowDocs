---
title: Security incident creation
description: Security incidents can be created manually from the form, or automatically via security events received from integrated third-party alert monitoring tools, such as Splunk.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security incident creation

Security incidents can be created manually from the form, or automatically via security events received from integrated third-party alert monitoring tools, such as Splunk.

**Important:** The latest features in Security Incident Response are exclusively available in the Security Incident Response Workspace. Install or upgrade to the latest Security Incident Response or Security Incident Response Workspace version to access and leverage features such as Shift-Handover, Risk Score Calculator, and so on.

If you have a security role, you can use any of the following methods to manually create security incidents.

<table id="table_b5j_jj1_ks"><thead><tr><th>

Method

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Manually created from the Security Incident list](../task/t_ManuallyCreateSecurityIncident.md)

</td><td>

On the Security Incident list, select **New** to create a new security incident.

</td></tr><tr><td>

[Manually created from the Security Incident Catalog](../task/manual-si-creation-catalog.md)

</td><td>

You can create security incidents by selecting from categories of security threats defined in the security incident catalog.

</td></tr><tr><td>

[Incident Management](https://www.servicenow.com/docs/access?context=c_IncidentManagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)

</td><td>

On the Incident form in incident management, select **Create Security Incident** to create a new security incident.**Note:** You can avoid duplicate security incidents creation by enabling the `sn_si.disable_duplicate_security_incident` system property.

</td></tr><tr><td>

[Manually converted from a security request](../task/t_CreateSecurityIncidentRequest.md)

</td><td>

On the Security Request form, select **Convert to Security Incident** to create a new security incident.

</td></tr><tr><td>

[Manually created from an Event Management alert](../task/manually-create-si-from-em-alert.md)

</td><td>

On the Event Management Alerts form, select **Create Security incident** to create a new security incident from an alert.

</td></tr><tr><td>

[Manually created from an alert](https://www.servicenow.com/docs/access?context=t_CreateAnAlertFromAnIncident&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)

</td><td>

On the Event Management Alert form, select **Create Security Incident** to create a new security incident.

</td></tr><tr><td>

Manually converted from a vulnerability record \(if the Vulnerability Response plugin is activated\)

</td><td>

On the Vulnerability Items form, select **Create Security Incident** to create a new security incident.

</td></tr></tbody>
</table>## Automatic creation of security incidents

Generally, security administrators are responsible for setting up alert rules to automatically generate security incidents.

|Method|Description|
|------|-----------|
|[Automatically created using alert rules](c_ScIncdUseAlrts.md)|Security incidents can be created based on alert rules defined in the [Event management in your data center](https://www.servicenow.com/docs/access?context=c_EM&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) application.|


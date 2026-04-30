---
title: Set up your ServiceNow AI Platform instance for the McAfee ePO integration
description: The following section lists the setup tasks that you’re required to complete in your ServiceNow AI Platform instance prior to installing the application for the McAfee ePO integration.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [McAfee ePO integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up your ServiceNow AI Platform instance for the McAfee ePO integration

The following section lists the setup tasks that you’re required to complete in your ServiceNow AI Platform® instance prior to installing the application for the McAfee ePO integration.

## Set up requirements

Role required: ServiceNow AI Platform administrator \(admin\). Review the following information before your ServiceNow AI Platform® instance for the McAfee ePO integration.

The following table is a list of setup requirements for the application. Verify that you’ve completed these tasks before you install the application for the integration from the ServiceNow Store.

<table id="table_hvr_2dr_2gb"><thead><tr><th>

Set up task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify that you’ve assigned the required ServiceNow AI Platform® and Security Incident Response \(SIR\) roles.

</td><td>

The following roles are required:-   A user with the system administrator \(admin\) role to install the application.
-   A user with the security incident administrator \(sn\_si.admin\) role configures the application, and creates, activates, and removes profiles.
-   A user with the security incident analyst \(sn\_si.analyst\) role works with security incidents. Tasks include manually launching profiles from security incidents. If the approval option is selected in a profile during the configuration step, users with this role also submit requests for isolating hosts and returning them to the network.

</td></tr><tr><td>

Verify that you are using version 5.9 of McAfee ePO.

</td><td>

The integration supports version 10.4.3 of the McAfee ePolicy Orchestrator.

</td></tr><tr><td>

Verify that you have installed the ServiceNow extension plugin in your McAfee ePO console.

</td><td>

Install the ServiceNow plugin in your McAfee ePO console. For more information and to obtain the plugin file, in your ServiceNow AI Platform instance, navigate to **Knowledge** &gt; **Articles** &gt; **All** and, in the Search field, enter, ServiceNow Security Operations Extension for McAfee ePO .

</td></tr><tr><td>

Verify that the ServiceNow core applications that are required to support the integration are installed and activated before you install the application for the integration.

</td><td>

Security Incident Response Dependency plugin \(com.snc.si\_dep\) is required. This plugin automatically installs all the dependencies that are required to support the Security Incident Response product. Install and activate this plugin before you install and activate the other Security Operations applications required by the integration.

 Verify that the following Security Operations applications are installed and activated from the ServiceNow Store. If not installed, install and activate one application at a time in the following order to ensure a smooth installation.

 1.  Security Incident Response
2.  Security Incident Response Workspace
3.  Security Integration Framework
4.  Security Support Common
5.  Security Support Orchestration

 For more information about installing the Security Operations core applications, see [Get entitlement for a Security Operations product or application](../../security-incident-response/task/entitle-secops-product.md) and [Activate a ServiceNow Store application](../../security-incident-response/task/activate-entitled-store-app.md).

</td></tr><tr><td>

Verify that you have installed and configured a MID Server.

</td><td>

An installed and configured MID Server is required in your ServiceNow AI Platform® instance. See the [ServiceNow Product Documentation website](https://servicenow.com/docs) for more information about MID Servers.

</td></tr><tr><td>

If you want to enable the approval process for profiles, verify that you have created an approval group to process requests.

</td><td>

There is an optional approval process available for isolating host machines and restoring them to the network.

If this option is enabled, prior approval is required before host machines are isolated and restored to your network.

If your organization wants an extra level of control over these actions, enable the **Require approval** option during the configuration step for a profile.

By default, approval authority is assigned to the ServiceNow AI Platform® security incident administrator \(sn\_si.admin\). This authority can be reassigned to an approval group. Within the group, any member has permission to approve or reject requests.You select an active approval group during the configuration step of your profile setup. For more information, see [Create an approval group](../task/create-approval-group-mcafee.md).

</td></tr></tbody>
</table>**Parent Topic:**[McAfee ePO integration](../concept/mcaffee-epo-overview-arch.md)

**Previous topic:**[Checklist for the McAfee ePO integration](../task/mcafee-epo_checklist.md)

**Next topic:**[Set up your McAfee ePO console to integrate with Security Incident Response \(SIR\)](../task/mcafee-epo-setup-mcafee.md)


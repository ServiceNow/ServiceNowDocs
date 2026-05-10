---
title: Configure Mobile Agent for Public Sector Digital Services
description: Configure Mobile Agent for the Information Request and Service Request Playbooks.Install the Customer Service Mobile and Information Request Playbook plugins to enable government agents to track public record information requests on the Mobile Agent. You can then configure the roles.Install the Customer Service Mobile and Service Request Playbook plugins to enable government service agents to track non-emergency service requests on the Mobile Agent. You can then configure the roles.Configure user roles for government service agents to access the Mobile Agent app. This step is mandatory for any government service agent to be able to work from the app.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Agent tools, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure Mobile Agent for Public Sector Digital Services

Configure Mobile Agent for the Information Request and Service Request Playbooks.

## Configure Mobile Agent for Information Request Playbook

Install the Customer Service Mobile and Information Request Playbook plugins to enable government agents to track public record information requests on the Mobile Agent. You can then configure the roles.

As an admin, complete the following configuration tasks to set up the Mobile Agent application.

<table id="table_cmk_mdm_fwb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Install Information Request Playbook application](../task/install-psds-information-request-playbook.md)

</td><td>

Install Information Request Playbook \(com.sn\_public\_sector\_digital\_services\_core\) from the ServiceNow® Store.

</td></tr><tr><td>

Activate the Customer Service Mobile plugin \(com.sn\_csm\_mobile\)

</td><td>

You can activate the Customer Service Mobile plugin \(com.sn\_csm\_mobile\) using the Customer Service Management guided setup.

</td></tr><tr><td>

[Configure public sector roles and permissions for Mobile Agent app](psds-config-mobile-agent.md#)

</td><td>

Configure user roles in order for government agents to access the Mobile Agent app. This step is mandatory for any government agent to be able to work from the app.

</td></tr></tbody>
</table>Once the Customer Service Management mobile application is activated and configured, agents can download the ServiceNow Mobile Agent on their mobile devices and access ServiceNow instances.

## Configure Mobile Agent for Service Request Playbook

Install the Customer Service Mobile and Service Request Playbook plugins to enable government service agents to track non-emergency service requests on the Mobile Agent. You can then configure the roles.

As a user with the admin role, complete the following configuration tasks to set up the Mobile Agent application.

<table id="table_cmk_mdm_fwb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Install Service Request Playbook application](../task/install-psds-service-request-playbook.md)

</td><td>

Install Service Request Playbook \(sn\_gsm\) from the ServiceNow® Store.

</td></tr><tr><td>

Activate the Customer Service Mobile plugin \(com.sn\_csm\_mobile\)

</td><td>

You can activate the Customer Service Mobile plugin \(com.sn\_csm\_mobile\) using the Customer Service Management guided setup.

</td></tr><tr><td>

\(Optional\) [Activate Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/t_ActivateFieldServiceManagement.md) plugin \(com.snc.work\_management\)

</td><td>

Install the Field Service Management plugin to view the work orders related list. For more information, see [Integration with Field Service Management](psds-integration-fsm.md).

</td></tr><tr><td>

[Configure public sector roles and permissions for Mobile Agent app](psds-config-mobile-agent.md#)

</td><td>

Configure user roles in order for government service agents to access the Mobile Agent app. This step is mandatory for any government service agent to be able to work from the app.

</td></tr></tbody>
</table>Once the Customer Service Management mobile application is activated and configured, agents can download the ServiceNow Mobile Agent on their mobile devices and access ServiceNow instances.

### Configure public sector roles and permissions for Mobile Agent app

Configure user roles for government service agents to access the Mobile Agent app. This step is mandatory for any government service agent to be able to work from the app.

#### Before you begin

Role required: admin

#### Procedure

1.  In the navigation filter, enter **sys\_sg\_applet\_launcher.list** to open the Applet Launchers \[sys\_sg\_applet\_launcher\] table.

2.  From the Launcher screens table, select the **Cases** record.

    The Required Roles record should contain only the Customer Service Agent \(sn\_customerservice\_agent\) role.

3.  If prompted, switch from the Global application to the Customer Service Mobile application.

4.  Select the edit icon \(![Edit icon.](../image/edit-icon.png)\) under Required Roles and add the following roles:

    -   sn\_gsm.agency\_manager
    -   sn\_gsm.government\_service\_manager
    -   sn\_gsm.constituent\_agent
    -   sn\_gsm.business\_agent
    -   sn\_gsm.agency\_constituent\_agent
    -   sn\_gsm.agency\_agent
5.  Select **Done** to save the roles.

    Agents with the above roles can now log in to the Mobile Agent and work on Service Request cases assigned to them.



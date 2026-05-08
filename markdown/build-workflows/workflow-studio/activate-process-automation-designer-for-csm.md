---
title: Activate Playbooks for Customer Service Management \(CSM\)
description: Activate Workflow Studio Playbooks on your instance so that you can create Playbooks triggered by CSM tables.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Activate Playbooks, Configure, Playbooks, Workflow Studio, Build workflows]
---

# Activate Playbooks for Customer Service Management \(CSM\)

Activate Workflow Studio Playbooks on your instance so that you can create Playbooks triggered by CSM tables.

## Before you begin

Role required: admin

## About this task

In order to create Playbooks in Workflow Studio that are triggered by CSM tables and custom tables that extend from them, you need to [purchase a subscription to CSM](https://www.servicenow.com/lpgp/pricing-csm.html).

To purchase this subscription, contact your ServiceNow account manager. Your account manager can arrange to have the plugin activated on your organization's production and subproduction instances, generally within a few days.

If you don't have an account manager, decide to delay activation after purchase, or want to evaluate the product on a subproduction instance without charge, follow these steps to enable the **Playbooks for Customer Service Management \[com.sn\_csm\_playbook\]** plugin:

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Select **Request plugin** to open the **Activate Plugin** form on Now Support.

3.  On the **Activate Plugin** form, provide the following information.

<table id="table_awx_bhf_ygb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="target-instance"><td>

What is your target instance

</td><td>

Select the instance that you want to activate the plugin on.

</td></tr><tr><td>

Which plugin would you like to activate

</td><td>

Select the name of the plugin to activate.

 **Note:** If the system doesn't list the plugin you want or if you're activating the plugin on an OEM or on-premise instance, select the **Plugin I'm looking for is not listed** check box and then enter the name of the plugin.

</td></tr><tr id="date-time"><td>

Select Maintenance Date and Time

</td><td>

Select the date and time to activate the plugin.

</td></tr></tbody>
</table>    For example, see the following form to activate the Event Management plugin on an instance named SNC Instance.

4.  Select **Submit**.

    After the maintenance window, the system installs the plugin on your instance. To confirm the installation, go to the Installed tab in the Application Manager.


## Result

Enabling the **Playbooks for Customer Service Management \[com.sn\_csm\_playbook\]** plugin lets you create playbooks for these tables and their extensions:

-   Account \[customer\_account\]
-   Case \[sn\_customerservice\_case\]
-   Change Request \[change\_request\]. Requires Customer Service with Service Management \(com.sn\_cs\_sm\)
-   Consumer \[csm\_consumer\]
-   Contact \[customer\_contact\]
-   Escalation \[sn\_customerservice\_escalation\]
-   Household \[csm\_household\]
-   Incident \[incident\]. Requires Customer Service with Service Management \(com.sn\_cs\_sm\)
-   Interaction \[interaction\]
-   Order \[csm\_order\]. Requires Customer Service Management for Orders \(com.snc.csm.order\)
-   Order Line Item \[csm\_order\_line\_item\]. Requires Customer Service Management for Orders \(com.snc.csm.order\)
-   Problem \[problem\]. Requires Customer Service with Service Management \(com.sn\_cs\_sm\)
-   Request \[sc\_request\]. Requires Customer Service with Request Management \(com.sn\_cs\_sm\_request\)
-   Service Organization \[sn\_customer\_service\_organization\]. Requires Service Organization \(com.snc.service\_organization\)
-   Task \[sn\_customerservice\_task\]

**Note:** If you create a custom table that extends a CSM table such as Case, you can create playbooks that trigger from it.

**Parent Topic:**[Activate Playbooks](../concept/activate-process-automation-designer.md)


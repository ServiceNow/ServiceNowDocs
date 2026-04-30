---
title: Add the Process tab to the portal
description: Add a Process tab to the CSM ticket page so that users can track the playbook process.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-04-15"
reading_time_minutes: 1
breadcrumb: [Set up predefined Playbooks for Portals, Playbooks for Portals, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Add the Process tab to the portal

Add a **Process** tab to the CSM ticket page so that users can track the playbook process.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Standard Ticket** &gt; **Standard Ticket Configuration**.

2.  Open the configuration for your table.

3.  In the **Tabs** related list, click **New**.

4.  In the **Tab Configuration** form, fill in the fields as follows.

    ![New tab configuration form](../image/tab-config.png "Tab Configuration form")

<table id="table_mpx_lrs_1fc"><thead><tr><th>

Field

</th><th>

Data

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Custom

</td></tr><tr><td>

Tab name

</td><td>

Process

</td></tr><tr><td>

Advanced

</td><td>

Toggle to active

</td></tr><tr><td>

Visible script

</td><td>

Add one or more playbook sysIds

</td></tr><tr><td>

Widget

</td><td>

Playbook

</td></tr><tr><td>

Widget parameters

</td><td>

Widget 1:

 Name: playbook\_uib\_page\_url

 Value: /now/playbook-portal/csm\_case\_process

 Widget 2:

 Name: playbook\_experience\_id

 Value: 0d71033773f220109edbc1f52ff6a741

</td></tr></tbody>
</table>5.  Select **Submit**.

    **Note:**

    For the user to view the process tabs in the portal, ensure you have assigned the requisite ACLs.



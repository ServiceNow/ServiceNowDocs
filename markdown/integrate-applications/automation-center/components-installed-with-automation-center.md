---
title: Components installed with Automation Center
description: Several types of components are installed with the activation of Automation Center, including tables, user roles, and scheduled jobs.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Automation Center, Workflow Data Fabric]
---

# Components installed with Automation Center

Several types of components are installed with the activation of Automation Center, including tables, user roles, and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Demo data is available for this plugin.

## Roles installed

**Note:** To view the Robotic Process Automation \(RPA\) data, RPA roles are required. For more information about RPA roles, see [Components installed with RPA Hub](../../rpa-hub/reference/installed-with-rpa-hub.md) .

<table id="table_ddp_3pg_wtb"><thead><tr><th>

Role title

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Automation admin \[sn\_ac.automation\_admin\]

</td><td>

Sets up Automation Center application configurations. Performs all the actions in the Automation Center application. Possesses CRUD access for all tables.

</td><td>

-   sn\_ac.automation\_business\_user
-   sn\_ac.automation\_technical\_user
-   sn\_ac.automation\_admin

</td></tr><tr><td>

Automation technical user \[sn\_ac.automation\_technical\_user\]

</td><td>

Creates automation requests, automation sources, automation tasks, automation resources, automation goals, insight rules, and insight triggers. Modifies automation attributes.

</td><td>

sn\_ac.automation\_techincal\_user

</td></tr><tr><td>

Automation business user \[sn\_ac.automation\_business\_user\]

</td><td>

Creates automation requests, automation goals, and updates the automation request life-cycle stages.

</td><td>

sn\_ac.automation\_business\_user

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_dx3_gb1_wdb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Automation Center: Purge Executions Data**

</td><td>

Deletes the data in the Automation Execution table only when the following conditions are met:

-   Records that were created ‘X’ days ago. X represents the value defined by the **sn\_ac.purge\_automation\_data\_in\_days** system property. Users with the automation admin role can modify this property value. The default value of this property is **14**.
-   Records with a state of **Cancelled**, **Complete**, or **Error**.

</td></tr><tr><td>

**Automation Center: Purge Insights Data**

</td><td>

Deletes the data in the **sn\_ac\_insight** system property that was created 'X' days ago. X represents the value defined by the **sn\_ac.purge\_automation\_data\_in\_days** system property. Users with the automation admin role can modify this property value. The default value provided of this property is **14**.

</td></tr><tr><td>

**Automation Center: Copy spotlight score into request**

</td><td>

**Note:** Available only if Spotlight is installed and enabled.

 Copies the spotlight score into the automation request’s Score field.

 The **Schedule \| Run to** is set to **On Demand**. It is recommended not to change this setting.

 **Note:** If you change the default spotlight criteria, then after saving the changes made, you must select the **Execute Now** button in this Spotlight group record to recompute the Spotlight score for the automation request records. And, then you must select the **Execute Now** button on the scheduled job to copy the score.

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Automation Request \[sn\_ac\_automation\_request\]

</td><td>

Contains the details of the automation request.

</td></tr><tr><td>

Automation Task \[sn\_ac\_automation\_task\]

</td><td>

Contains information of tasks linked to a request.

</td></tr><tr><td>

Automation Goal \[sn\_sc\_automation\_goal\]

</td><td>

Contains details of goals that can be mapped to multiple requests.

</td></tr><tr><td>

Base Robot \[cmdb\_ci\_base\_rpa\_robot\]

</td><td>

Contains the details of a software agent that runs a bot process.

</td></tr><tr><td>

Base Bot Process \[cmdb\_ci\_base\_rpa\_process\]

</td><td>

Contains the configuration details of a robot.

</td></tr><tr><td>

Automation Execution \[sn\_ac\_automation\_execution\]

</td><td>

Stores all execution processes information.

</td></tr><tr><td>

Automation Insight\[sn\_ac\_insight\]

</td><td>

Contains alerts data across Automation Center.

</td></tr><tr><td>

Automation Insight rule\[sn\_ac\_insight\_rule\]

</td><td>

Contains rules that configure insights.

</td></tr><tr><td>

Automation Source \[sn\_ac\_automation\_source\]

</td><td>

Stores vendor data.

</td></tr><tr><td>

Automation Attribute\[sn\_ac\_ci\_attribute\]

</td><td>

Stores cost, time, source, and associated automation for processes and robot.

</td></tr><tr><td>

Automation Import \[sn\_ac\_rpa\_import\]

</td><td>

Temporarily stores data that is imported from the REST API.

</td></tr></tbody>
</table>**Parent Topic:**[Automation Center reference](../concept/automation-center-reference.md)


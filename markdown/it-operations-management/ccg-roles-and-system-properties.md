---
title: Cloud Configuration Governance roles and system properties
description: Cloud Configuration Governance users require the appropriate roles and system properties to perform various activities. These roles and system properties are installed with the activation of the application.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Cloud Configuration Governance reference, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud Configuration Governance roles and system properties

Cloud Configuration Governance users require the appropriate roles and system properties to perform various activities. These roles and system properties are installed with the activation of the application.

Only users with the user\_admin or admin role can create users with these roles.

<table id="table_en1_jf1_bsb"><thead><tr><th align="left">

Name

</th><th align="left">

Responsibility

</th><th>

Nested roles

</th></tr></thead><tbody><tr><td>

sn\_itom\_ccg.scheduling\_admin

</td><td>

A scheduling admin can perform the following actions:-   Create scan schedules.
-   Create CI finder mappings.

</td><td>

discovery\_admin

</td></tr><tr><td>

sn\_itom\_ccg.governor

</td><td>

A governor can perform the following actions:-   Create policies by using condition builder, Integration Hub flows, or script.
-   Create a policy set.
-   Create resource collectors.
-   Create configuration keys.
-   Create remediation.
-   Create CI finder mappings.

</td><td>

-   flow\_designer
-   action\_designer
-   catalog\_admin

</td></tr><tr><td>

sn\_itom\_ccg.ccg\_operator

</td><td>

An operator can perform the following actions:-   View the audit issue reports.
-   Run remediation.
-   Run scan configurations.
-   View the dashboard.

</td><td>

-   flow\_operator
-   sn\_change\_write

</td></tr><tr><td>

sn\_itom\_ccg.report\_viewer

</td><td>

A report viewer can perform the following actions:-   View the audit issue reports.
-   View the dashboard.

</td><td>

 

</td></tr></tbody>
</table><table id="table_l4p_5q1_bsb"><thead><tr><th align="left">

Property name

</th><th align="left">

Description

</th></tr></thead><tbody><tr><td>

**snc\_af.log\_level**

</td><td>

When you enable this property, Cloud Configuration Governance writes the logs to the syslog.The supported logging levels are as follows:

-   DEBUG
-   INFO
-   WARN
-   ERROR
-   OFF

 Ensure that the application scope is **Global**, when you set or clear this property.

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Configuration Governance reference](../reference/ccg-reference.md)

**Related topics**  


[Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)


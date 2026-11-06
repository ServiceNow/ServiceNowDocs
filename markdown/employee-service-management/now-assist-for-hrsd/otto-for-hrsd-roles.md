---
title: Otto for HRSD Roles
description: These roles control who can administer and use generative AI, AI agents, Voice, and Galileo features.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/now-assist-for-hrsd/otto-for-hrsd-roles.html
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: reference
last_updated: "2026-10-15"
reading_time_minutes: 1
breadcrumb: [Reference, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Otto for HRSD Roles

These roles control who can administer and use generative AI, AI agents, Voice, and Galileo features.

## Roles

The following table lists the roles required to configure and use the AI features in HR Service Delivery \(HRSD\) applications. Administrators must be assigned the relevant roles to configure each feature. HR agents can use the generative AI features without any additional roles.

<table id="table-otto-hrsd-roles"><thead><tr><th>

User persona

</th><th>

Role

</th><th>

Description

</th><th>

Plugin

</th></tr></thead><tbody><tr><td>

Admin

</td><td>

`sn_hr_gen_ai.admin`

</td><td>

Configures generative AI features

 Is auto-assigned to the `sn_hr_core.admin` role.

</td><td>

ServiceNow Otto for HR Service Delivery \(HRSD\)\[sn\_hr\_gen\_ai\]

</td></tr><tr><td>

Admin

</td><td>

`sn_hr_ai_agents.admin`

</td><td>

Configures AI Agents and runs the readiness report

</td><td>

AI Agents for HR Service Delivery\[sn\_hr\_ai\_agents\]

</td></tr><tr><td>

Admin

</td><td>

`sn_hr_voice_aia.admin`

</td><td>

Provides access to HRSD Voice agent configuration flow

</td><td>

HR Voice AI Agents \[sn\_hr\_voice\_aia\]

</td></tr><tr><td>

Admin

</td><td>

`sn_hr_na_galileo.admin`

</td><td>

Is auto-assigned to the `sn_hr_gen_ai.admin` role.

 Grants administrative access to the Galileo data store.

</td><td>

ServiceNow Otto for HRSD – Galileo Inside\[sn\_hr\_na\_galileo\]

</td></tr><tr><td>

HR agent

</td><td>

`sn_hr_na_galileo.read`

</td><td>

Enables users to receive Now Assist responses containing Galileo data

</td><td>

ServiceNow Otto for HRSD – Galileo Inside\[sn\_hr\_na\_galileo\]

</td></tr><tr><td>

Employee

</td><td>

sn\_voice\_aia.guest

</td><td>

Enables employees to use AI voice agents without authentication

</td><td>

HR Voice AI Agents \[sn\_hr\_voice\_aia\]

</td></tr></tbody>
</table>**Parent Topic:**[Reference for ServiceNow Otto for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/now-assist-for-hrsd/reference-now-assist-hrsd.md)


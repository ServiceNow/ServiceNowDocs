---
title: Service Desk Manager role in SOW for ITSM
description: The IT Service Management for AI Agent Collection plugin\[sn\_itsm\_aia\] installs Service Desk Manager and AI Worker roles when activated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/roles-required-l1-sd-ai-spec.html
release: australia
topic_type: reference
last_updated: "2026-08-25"
reading_time_minutes: 1
breadcrumb: [Reference, L1 IT Service Desk AI Specialist, IT Service Management]
---

# Service Desk Manager role in SOW for ITSM

The IT Service Management for AI Agent Collection plugin\[sn\_itsm\_aia\] installs Service Desk Manager and AI Worker roles when activated.

The following roles are available with the installation of the IT Service Management for AI Agent Collection \[sn\_itsm\_aia\] 5.1.

<table id="table_hpq_zvc_yhc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Service Desk Manager \[sn\_itsm\_common.sn\_service\_desk\_manager\]

</td><td>

Extends the capabilities of standard Service Desk Agent \(sn\_service\_desk\_agent\) role by enabling efficient team oversight and incident resolution without requiring full administrative access.

 Can also onboard any available L1 IT Service Desk AI Specialist to the team.

</td><td>

-   sn\_service\_desk\_agent
-   sn\_aia.worker\_manager

</td></tr><tr><td>

AI Worker Manager \[sn\_aia.worker\_manager\]

</td><td>

Can activate, onboard, setup any available L1 IT Service Desk AI Specialist to the team from the SOW Landing page or AI Agent Studio.

</td><td>

None

</td></tr></tbody>
</table>
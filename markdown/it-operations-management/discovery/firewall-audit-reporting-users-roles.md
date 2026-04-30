---
title: Firewall Audits and Reporting roles and responsibilities
description: Specific users and roles to optimize the monitoring and tracking of requests for new firewall rules.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring Firewall Audits and Reporting, Firewall Audits and Reporting, Discovery, ITOM Visibility, IT Operations Management]
---

# Firewall Audits and Reporting roles and responsibilities

Specific users and roles to optimize the monitoring and tracking of requests for new firewall rules.

The configuration settings are activated or deactivated depending on the assigned roles.

<table id="table_o1v_pbq_31c"><thead><tr><th>

Role

</th><th>

Responsibilities

</th></tr></thead><tbody><tr><td>

Firewall Admin \[sn\_disco\_firewall.firewall\_admin\]

</td><td>

Responsible for editing Configuration Item \(CI\) attributes not populated by Discovery, including "assigned\_to" and others. Firewall Admins possess the capability to view the Firewall managers list with specific details for each manager. Furthermore, they have the authority to view and edit the dashboard, initiate audits from the firewall manager details page, create, modify, and view policies, edit audit tasks, and request policy changes.**Note:** The Firewall Admin role includes the Firewall User role. This role is not automatically granted with the discovery\_admin role and needs to be explicitly assigned to the user.

</td></tr><tr><td>

Firewall User\[sn\_disco\_firewall.firewall\_user\]

</td><td>

Responsible for viewing firewall dashboards and policies in a Read-only capacity.**Note:** This role includes the Firewall Requester role.

</td></tr><tr><td>

Firewall Requester \[sn\_disco\_firewall.firewall\_requester\]

</td><td>

Responsible for requesting new firewall rules through the Service Catalog.

</td></tr></tbody>
</table>
---
title: Components installed with Common Service Delivery
description: Several types of components are installed with the installation of the Common Service Delivery application, including tables and user roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/common-service-delivery/installed-with-common-service-delivery.html
release: australia
product: Common Service Delivery
classification: common-service-delivery
topic_type: reference
last_updated: "2026-08-06"
reading_time_minutes: 1
breadcrumb: [Learn about FSC common applications, Common applications, Finance and Supply Chain applications, Finance and Supply Chain]
---

# Components installed with Common Service Delivery

Several types of components are installed with the installation of the Common Service Delivery application, including tables and user roles.

## Roles installed

<table id="table_roles_csd"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Common Service Delivery admin\[sn\_spend\_sdc.admin\]

</td><td>

Role required to access Service Task and Service Request tables, which extends to Procurement Case Management, as well as other infrastructure that forms the foundation of Finance and Supply Chain Workflows products.

</td><td>

None

</td></tr><tr><td>

Common Service Delivery requestor\[sn\_spend\_sdc.requestor\]

</td><td>

Create and track finance cases and case lines that you submitted.

</td><td>

None

</td></tr><tr><td>

Common Service Delivery agent\[sn\_spend\_sdc.agent\]

</td><td>

Work finance cases and finance tasks assigned to you, including composing email responses and using response templates.

</td><td>

sn\_templated\_snip.template\_snippet\_reader, email\_composer

</td></tr><tr><td>

Common Service Delivery manager\[sn\_spend\_sdc.manager\]

</td><td>

Manage and oversee finance cases and finance tasks, including all agent capabilities.

</td><td>

sn\_spend\_sdc.agent

</td></tr></tbody>
</table>## Tables installed

<table id="table_tables_csd"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Finance Case\[sn\_spend\_sdc\_service\_request\]

</td><td>

Stores finance and procurement case records, such as purchase order edits, returns, GL coding reviews, budget reviews, and supplier-related requests, along with the case state and related records.

</td></tr><tr><td>

Finance Case Line\[sn\_spend\_sdc\_service\_request\_line\]

</td><td>

Stores line-level details of a finance case, including quantity, budget, and modification information for the associated case.

</td></tr><tr><td>

Finance Task\[sn\_spend\_sdc\_service\_task\]

</td><td>

Stores task records associated with a finance case, including supplier, instructions, and document or survey signature details.

</td></tr><tr><td>

Playbook status\[sn\_spend\_sdc\_playbook\_status\]

</td><td>

Maps a playbook activity to the status text displayed on the playbook stepper, including the status to show if the activity is skipped or canceled.

</td></tr><tr><td>

Procurement Exception\[sn\_spend\_sdc\_exception\]

</td><td>

Extends the Finance Case table to track procurement exceptions raised manually, by email, by an AI agent, or through ERP integration, including the root cause and resolution notes.

</td></tr><tr><td>

Case Exclusion Rule\[sn\_spend\_sdc\_case\_exclusion\_rule\]

</td><td>

Defines the case types, such as invoice inquiry cases, that are excluded from evaluation by a finance case exclusion rule.

</td></tr></tbody>
</table>
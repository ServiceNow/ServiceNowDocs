---
title: Components installed with Lead Management
description: Several types of components are installed with activation of the Lead Management plugin, including tables and user roles.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Lead Management reference, Lead and opportunity management, Reference, Sales Customer Relationship Management]
---

# Components installed with Lead Management

Several types of components are installed with activation of the Lead Management plugin, including tables and user roles.

## Roles installed

<table id="table_rt5_bzl_nhc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Lead writer \[sn\_lead\_mgmt\_core.lead\_writer\]

</td><td>

A granular role created to give write access to Lead and Lead Line Item.

</td><td>

sn\_lead\_mgmt\_core.lead\_viewer

</td></tr><tr><td>

Lead integrator \[sn\_lead\_mgmt\_core.lead\_integrator\]

</td><td>

Lead integrator have access to call the REST APIs of lead.

</td><td>

sn\_lead\_mgmt\_core.lead\_writer

</td></tr><tr><td>

Lead responsibility write granular \[sn\_lead\_mgmt\_core.lead\_responsibility\_write\_granular\]

</td><td>

Provides granular access to lead and related entities through the responsibility framework.

</td><td>

sn\_lead\_mgmt\_core.lead\_responsibility\_read\_granular

</td></tr><tr><td>

Lead responsibility read granular \[sn\_lead\_mgmt\_core.lead\_responsibility\_read\_granular\]

</td><td>

Provides granular read-only access to lead and its related entities through the responsibility framework.

</td><td>

None

</td></tr><tr><td>

Lead agent \[sn\_lead\_mgmt\_core.lead\_agent\]

</td><td>

Lead agent can perform CRUD operations on Lead and related tables.

</td><td>

-   sn\_customerservice.csm\_workspace\_user
-   sn\_lead\_mgmt\_core.lead\_writer

</td></tr><tr><td>

Lead admin \[sn\_lead\_mgmt\_core.lead\_admin\]

</td><td>

An admin role created to give create, update, read, and delete access on lead tables.

</td><td>

-   sn\_lead\_mgmt\_core.lead\_agent
-   sn\_lead\_mgmt\_core.lead\_integrator

</td></tr><tr><td>

Lead viewer \[sn\_lead\_mgmt\_core.lead\_viewer\]

</td><td>

A granular role created to give read access to Lead and Lead Line Item.

</td><td>

-   sn\_csm\_ctxrul\_mgt.context\_variable\_viewer
-   sn\_prd\_pm.product\_catalog\_viewer
-   canvas\_user
-   sn\_csm\_ctxrul\_mgt.rule\_matrix\_viewer

</td></tr></tbody>
</table>## Tables installed

<table id="table_hqn_hjk_phc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Lead Needs

 sn\_lead\_mgmt\_lead\_needs

</td><td>

Specific requirements or expectations of a customer.

</td></tr><tr><td>

Lead Line Item

 sn\_lead\_mgmt\_core\_lead\_line\_item

</td><td>

Individual product entry within a lead.

</td></tr><tr><td>

Lead Task

 sn\_lead\_mgmt\_core\_lead\_task

</td><td>

A specific action or activity assigned to manage or progress a lead, such as follow-up calls, sending proposals, or scheduling meetings.

</td></tr><tr><td>

Lead

 sn\_lead\_mgmt\_core\_lead

</td><td>

Prospective customers who have expressed their interest through various channels, such as website forms, social media, or events.

</td></tr></tbody>
</table>**Parent Topic:**[Lead Management reference](../concept/lead-management-reference.md)


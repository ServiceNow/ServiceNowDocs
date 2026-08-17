---
title: Access limitations for external location consumer agents
description: Explore the limitations that an external location consumer agent \(having sn\_customerservice.svc\_location\_consumer\_agent and snc\_external roles\) faces when using various platform modules during case resolution. You can use this topic to get a comprehensive overview of the modules that are supported and unsupported with the external location consumer agent persona.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/access-limitations-for-ext-loc-customer-agent.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [external location customer agents]
breadcrumb: [External Organization as a fulfiller, Cases, Overview, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Access limitations for external location consumer agents

Explore the limitations that an external location consumer agent \(having sn\_customerservice.svc\_location\_consumer\_agent and snc\_external roles\) faces when using various platform modules during case resolution. You can use this topic to get a comprehensive overview of the modules that are supported and unsupported with the external location consumer agent persona.

**Important:** Some table and field labels have been changed across recent releases. For a mapping of former labels to current labels, see [Service Model Foundation renamed Entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/renamed-entities.md).

## Supported and unsupported modules

List of modules and submodules under the consumer service platform that are supported and unsupported:

<table id="table_fjn_lyd_ybc"><thead><tr><th>

Modules

</th><th>

Submodules

</th><th>

Supported/unsupported

</th></tr></thead><tbody><tr><td>

Overview

</td><td>

 

</td><td>

Supported

</td></tr><tr><td>

Knowledge

</td><td>

 

</td><td>

Supported

</td></tr><tr><td rowspan="8">

Cases

</td><td>

Create New

</td><td rowspan="8">

Supported

</td></tr><tr><td>

My Cases

</td></tr><tr><td>

Assigned to My Locations

</td></tr><tr><td>

Requested by My Locations

</td></tr><tr><td>

All

</td></tr><tr><td>

Open

</td></tr><tr><td>

Unassigned

</td></tr><tr><td>

Escalated

</td></tr><tr><td rowspan="2">

Customer

</td><td>

Consumer

</td><td rowspan="2">

Supported

</td></tr><tr><td>

Households

</td></tr><tr><td rowspan="2">

Customer Relationships

</td><td>

Consumer Team Members

</td><td rowspan="2">

Supported

</td></tr><tr><td>

Household Team Members

</td></tr><tr><td rowspan="3">

Business Organizations

</td><td>

Internal Organizations \(formerly Internal Business Locations\)

</td><td rowspan="3">

Supported

</td></tr><tr><td>

External Organizations \(formerly External Business Locations\)

</td></tr><tr><td>

External Organization Staff \(formerly Service Organization External Staffs\)

</td></tr><tr><td>

Workspaces

</td><td>

CSM Configurable Workspace

</td><td>

Unsupported**Note:** All aspects of the workspace experience remain inaccessible to external location agents.

</td></tr></tbody>
</table>The Launch Interactive Analysis option in the Case list form context menu isn’t functional.

With an external organization as a fulfiller, you can create and manage cases for the households, and consumers from the platform. For more information on how to create and manage cases, see [Create and manage cases for a business organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/manage-business-location-cases.md).


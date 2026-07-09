---
title: Components installed with Buying Group
description: Several types of components are installed with activation of the Buying Group\[var.buying-group\] plugin, including user roles and tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/components-installed-buying-group.html
release: australia
topic_type: reference
last_updated: "2026-06-13"
reading_time_minutes: 1
breadcrumb: [Lead and opportunity management, Reference, Sales Customer Relationship Management]
---

# Components installed with Buying Group

Several types of components are installed with activation of the Buying Group\[var.buying-group\] plugin, including user roles and tables.

## Roles installed

<table id="table_roles"><thead><tr><th>

Role name

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_buying\_group.bg\_viewer

</td><td>

Provides read access to buying groups and buying group members.

</td><td>

None

</td></tr><tr><td>

sn\_buying\_group.bg\_writer

</td><td>

Provides write access to buying groups and buying group members, including the ability to create, update, and delete records.

</td><td>

sn\_buying\_group.bg\_viewer

</td></tr></tbody>
</table>## Tables installed

<table id="table_tables"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Buying Group

 \[sn\_buying\_group\_buying\_group\]

</td><td>

A stakeholder committee associated with a customer account and product offering family, representing all individuals involved in a purchase decision.

</td></tr><tr><td>

Buying Group Member

 \[sn\_buying\_group\_member\]

</td><td>

A contact or lead associated with a buying group, along with their role and engagement details within the purchasing committee.

</td></tr><tr><td>

Buying Group Stage

 \[sn\_buying\_group\_stage\]

</td><td>

Configuration records that define the lifecycle stages of a buying group, such as Identified, Targeted, Qualified, In-Sales Motion, and Closed.

</td></tr><tr><td>

Opportunity Buying Group

 \[sn\_buying\_group\_opportunity\_buying\_group\]

</td><td>

Association records that link buying groups to opportunities, enabling sellers to connect a purchasing committee to one or more active deals.

</td></tr></tbody>
</table>**Parent Topic:**[Lead and opportunity management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/reference-lead-opportunity-mgt.md)


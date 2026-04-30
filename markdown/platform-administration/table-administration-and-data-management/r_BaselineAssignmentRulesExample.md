---
title: Baseline assignment rules example
description: A baseline instance contains certain assignment rules.
locale: en-US
release: yokohama
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Assignment rules, Work with the Task table, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Baseline assignment rules example

A baseline instance contains certain assignment rules.

<table id="table_cz3_xvh_fq"><thead><tr><th>

Name

</th><th>

Table

</th><th>

Conditions

</th><th>

Assigned to user, Assigned to group, or Script

</th></tr></thead><tbody><tr><td>

Networking

</td><td>

incident

</td><td>

Category is Network

</td><td>

User: System Administrator

 Group: Network

</td></tr><tr><td>

Database or Software

</td><td>

incident

</td><td>

Category is one of Request, Inquiry / Help, Software, Hardware

</td><td>

User: System Administrator

 Group: Software

</td></tr><tr><td>

SC Item fulfillment - Field Services

</td><td>

Ticket

</td><td>

Parent.Task type is Request item

</td><td>

Group: Field Services

</td></tr><tr><td>

Release Planning

</td><td>

release\_phase

</td><td>

Name is Plan

</td><td>

Script:```
current.release.product.service.assigned_to;
```

</td></tr><tr><td>

IT Hardware

</td><td>

sc\_req\_item

</td><td>

Approval is Approved and Item.Category is Request Computers and Hardware

</td><td>

User: System Administrator

 Group: Hardware

</td></tr><tr><td>

Service Desk

</td><td>

incident

</td><td>

Active is true

</td><td>

Group: Service Desk

</td></tr></tbody>
</table>**Parent Topic:**[Defining assignment rules](../concept/c_DefineAssignmentRules.md)

**Related topics**  


[Assignment rules module](../concept/c_AssignmentRulesModule.md)

[Data lookup rules](../concept/c_DataLookupRules.md)

[Precedence between data lookup, assignment, and business rules](../concept/c_PrecBetweenAssignmentAndBusRules.md)

[Workflow assignments](../concept/c_WorkflowAssignments.md)

[Create an assignment rule](../task/t_AssignmentModuleRule.md)

[Create an assignment data lookup rule](../task/t_DataLookupRule.md)


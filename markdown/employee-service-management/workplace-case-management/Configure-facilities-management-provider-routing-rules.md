---
title: Configure provider routing rules
description: Provider Routing Rules determine which workplace cases and tasks are sent to which FM providers. Rules use standard ServiceNow condition builders to evaluate case attributes.
locale: en-US
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setup Integrated Facilities Management Integration Framework, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Configure provider routing rules

Provider Routing Rules determine which workplace cases and tasks are sent to which FM providers. Rules use standard ServiceNow condition builders to evaluate case attributes.

## Before you begin

Role required: sn\_wsd\_case.manager

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Facilities Management - Setup** &gt; **Provider routing rules**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_qcy_zrc_f3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider

</td><td>

The FM Provider this rule routes to.

</td></tr><tr><td>

Active

</td><td>

Indicates if the rule is currently active.

</td></tr><tr><td>

Order

</td><td>

The priority sequence number that determines when this rule is evaluated relative to other routing rules. Routing rules are prioritized as follows:-   Order field \(in ascending order, with lower numbers given higher priority\)
-   Provider creation date \(providers created earlier are prioritized\)
-   Rule creation date \(rules created earlier are prioritized\)


</td></tr><tr><td>

Table

</td><td>

The ServiceNow table that this routing rule applies to. This defines which record types will be evaluated against this rule. For example, Workplace Case \[sn\_wsd\_case\_workplace\_case\].

</td></tr><tr><td>

Condition

</td><td>

The criteria that must be met for this routing rule to match and apply to a workplace case or task. Use the AND, OR condition builder to define one or more conditions based on field values such as service type, location, building, or any other workplace case fields. The system evaluates these conditions against incoming workplace cases to determine provider routing. For example, \[Workplace service\] \[is\] \[Cleaning\].

</td></tr></tbody>
</table>4.  Select **Submit**.


## Example

![](../../workplace-service-delivery/images/FM-provider-routing-rule.png)

## Route the case to Provider B when the workplace service is Heating &amp; Cooling and the location is Building A

![](../../workplace-service-delivery/images/Routing-rule-exmpl2.png)![](../../workplace-service-delivery/images/Routing-rule-exple1.png)


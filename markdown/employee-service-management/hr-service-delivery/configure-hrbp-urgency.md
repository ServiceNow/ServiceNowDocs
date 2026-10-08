---
title: Configure HRBP urgency rules
description: Create urgency rules to set a minimum urgency for HR cases that meet specific conditions, or describe urgency criteria for the AI to use during the enrichment process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/configure-hrbp-urgency.html
release: brazil
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 2
breadcrumb: [Configure, HRBP productivity assistant, HR Service Delivery, Employee Service Management]
---

# Configure HRBP urgency rules

Create urgency rules to set a minimum urgency for HR cases that meet specific conditions, or describe urgency criteria for the AI to use during the enrichment process.

## Before you begin

Role required: HRBP administrator \[sn\_hrbp\_hub.admin\]

## About this task

The enrichment process evaluates active urgency rules for active HR cases that are assigned to an HRBP. You can create two types of rules:

-   **Condition-based**

    If a case meets the rule's conditions, the enrichment process sets its urgency to at least the level you choose.

-   **Prompt-based**

    The AI evaluates the case against your natural language rule. Because AI output can vary, the case might not receive the level you choose. Review cases that a prompt-based rule applies to.


If more than one rule applies, the enrichment process uses the highest urgency level. For information on the rules available in the base system, see [HR case urgency rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/hr-case-urgency-rules.md).

## Procedure

1.  Navigate to **All** &gt; **HRBP Productivity** &gt; **Administration** &gt; **Urgency Rules**.

2.  Select **New**.

3.  Fill in the fields on the form.

<table id="table_scope_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Rule name

</td><td>

Name of the urgency rule.

</td></tr><tr><td>

Description

</td><td>

Explains what the rule does.

</td></tr><tr><td>

Rule type

</td><td>

Determines how the enrichment process evaluates the rule. Options: **None \(default\)**, **Condition-based**, **Prompt-based**.

A rule with **None** selected doesn't apply to any case.

</td></tr><tr><td>

Urgency level

</td><td>

Minimum urgency for cases that meet a condition-based rule. For a prompt-based rule, the urgency that the AI evaluates the case against.Options: **Critical**, **High**, **Medium**, **Low**.

</td></tr><tr><td>

Active

</td><td>

Option to activate the rule when the enrichment process runs.Selected by default.

</td></tr><tr><td>

Condition table

</td><td>

Table the rule evaluates. Defaults to HR Case \[sn\_hr\_core\_case\]. The rule checks the HR case itself, so select HR Case or a table that extends it.Appears only when Rule type is **Condition-based**.

</td></tr><tr><td>

Condition

</td><td>

Criteria that a case must meet for the rule to apply. Add criteria with **AND** and **OR**, or add a separate set with **New Criteria**. If you don't add criteria, the rule doesn't apply to any case.Appears only when Rule type is **Condition-based**.

</td></tr><tr><td>

Natural language rule

</td><td>

Plain-language description of when a case should get the selected urgency. The AI evaluates each case against this description.Appears only when Rule type is **Prompt-based**.

</td></tr></tbody>
</table>4.  Select **Submit**.

    The rule applies the next time the enrichment process runs for a case.



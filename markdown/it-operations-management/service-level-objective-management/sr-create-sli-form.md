---
title: Create SLI form
description: Learn about the available fields for adding a service level indicator \(SLI\) to a service level objective \(SLO\).
locale: en-US
release: yokohama
product: Service Level Objective Management
classification: service-level-objective-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SLO Management reference, Service Level Objective Management, ITOM AIOps, IT Operations Management]
---

# Create SLI form

Learn about the available fields for adding a service level indicator \(SLI\) to a service level objective \(SLO\).

## Add SLI form

The following table describes the available options in the Add SLI form. For step-by-step instructions, see [Create SLOs, SLIs, and error budget policies](../../slo-management/task/sr-create-slo-sli.md).

<table id="table_rqy_bnq_ybc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SLI name

</td><td>

Enter a name for your SLI. For example, Critical router issue.

</td></tr><tr><td>

Data source

</td><td>

This field is auto-populated.The alerts from this data source, also known as integration, are used to calculate the error budget.

</td></tr><tr><td colspan="2">

Set conditions \(optional\)Customize your SLI by filtering it to specific configuration items or alerts. The fields in this section are optional.

</td></tr><tr><td>

Filter by CI

</td><td>

Filter your SLI to a configuration item \(CI\) within the parent service's hierarchy. Filtering an SLI to a CI can help you more accurately track service health and identify root causes faster.

</td></tr><tr><td>

Add condition set

</td><td>

Select this option to specify the alerts included in the error budget.For example, if you set the condition to **Status is Critical**, only alerts with a critical status count toward the error budget.

</td></tr></tbody>
</table>**Parent Topic:**[SLO Management reference](../../slo-management/reference/service-level-objective-management-reference.md)


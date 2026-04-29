---
title: Create SLI form
description: Learn about the available fields for adding a service level indicator \(SLI\) to a service level objective \(SLO\).
locale: en-US
release: australia
product: Service Level Objective Management
classification: service-level-objective-management
topic_type: reference
last_updated: "2026-03-12"
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

This field is auto-populated.The alerts or outages are used to calculate the error budget.

</td></tr><tr><td>

Service or configuration item

</td><td>

-   &lt;Service-name&gt; - Select this option to filter your SLI to the entire service. This option helps you measure overall service health.
-   Related configuration item - If your service includes one or more configuration items \(CIs\) in its hierarchy, select this option to filter your SLI to specific CIs. This option provides a more granular view of service health.

 **Note:** By default, only level-one CIs appear in the CI list. Administrators can change the number of levels displayed by updating the `sn_sow_slo.slo_rollup_depth` system property value.

</td></tr><tr><td colspan="2">

Set conditions \(optional\)Customize your SLI by filtering it to specific alerts or outages. The fields in this section are optional.

</td></tr><tr><td>

Add condition set

</td><td>

Select this option to specify the alerts or outages included in the error budget.For example, for alerts, if you set the condition to **Status is Critical**, only alerts with a critical status count toward the error budget.

</td></tr></tbody>
</table>**Parent Topic:**[SLO Management reference](../../slo-management/reference/service-level-objective-management-reference.md)


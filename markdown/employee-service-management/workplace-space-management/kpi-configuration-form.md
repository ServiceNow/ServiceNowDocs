---
title: KPI Configuration form
description: The KPI Configuration form helps you create a key performance indicator for the Space Planning module in Workplace Central.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-space-management/kpi-configuration-form.html
release: australia
product: Workplace Space Management
classification: workplace-space-management
topic_type: reference
last_updated: "2026-05-18"
reading_time_minutes: 2
breadcrumb: [Reference, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# KPI Configuration form

The KPI Configuration form helps you create a key performance indicator for the Space Planning module in Workplace Central.

<table id="table_kpi_config_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the KPI Configuration.

</td></tr><tr><td>

Label

</td><td>

Display label that appears in the Space Planning workspace.

</td></tr><tr><td>

Application

</td><td>

Application scope in which the KPI Configuration record is created. The field is automatically filled based on the current application scope and can't be edited.

</td></tr><tr><td>

Active

</td><td>

Option to activate the record. When this field is selected, the KPI is calculated and displayed in the Space Planning workspace.

</td></tr><tr><td>

Order

</td><td>

Order of the KPI in the side panel. In the details panel, lower order values appear before the higher order values.

</td></tr><tr><td>

Description

</td><td>

Description that appears on a tooltip in the Space Planning workspace.

</td></tr><tr><td>

Type

</td><td>

The operation that is applied to the selected field. The operation is applied across all applicable spaces on the Space Planning workspace.Select one of the following values:

-   **SUM**: Calculates the sum of the values of the selected field.
-   **AVG**: Calculates the average of the values of the selected field.
-   **COUNT**: Counts the number of values of the selected field.
-   **COUNT DISTINCT**: Counts the number of unique values of the selected field.

For example, SUM of Capacity displays the total capacity of the applicable spaces.

**Note:**

For KPIs that require multiple operations, you can set the type to **None** and create a script include to calculate the value. To create a script include, you can create an implementation by using the `sn_wsd_spcmgmt.KPICustomConfig` extension point.

For reference, you can view the Script Includes like `KPI_profiles_assigned` or `KPI_assignment_ratio`, which are included with Workplace Space Management.

For more information about extension points, see [Using extension points to extend application functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/extension-points.md).

</td></tr><tr><td>

Computation field

</td><td>

Field on the Space \[sn\_wsd\_core\_space\] table on which the selected operation is performed. This field is displayed only after you select a value in the **Type** field.For example, SUM of Capacity displays the total capacity of the applicable spaces.

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Space Management references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-space-management/workplace-space-mgmt-references.md)

**Related topics**  


[Components installed with Workplace Space Management]()

[Properties installed with Workplace Space Management]()

[View by Configuration form]()


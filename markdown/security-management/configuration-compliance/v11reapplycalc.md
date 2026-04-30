---
title: Create, edit, and reapply risk calculators for Configuration Compliance
description: Calculator rules can be applied to all affected test results and collections on-demand. Vulnerability managers may use this feature adjust their risk calculator configuration and apply changes on-demand to import findings.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuration Compliance calculators and calculator rules, Create a Configuration Compliance calculator group, Configure, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Create, edit, and reapply risk calculators for Configuration Compliance

Calculator rules can be applied to all affected test results and collections on-demand. Vulnerability managers may use this feature adjust their risk calculator configuration and apply changes on-demand to import findings.

## Before you begin

Role required: sn\_vulc.admin

## Procedure

1.  To create a new risk calculator, follow these steps.

    1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Administration** and select **Risk Calculators**.

    2.  In the Risk Calculator list, click **New**.

    3.  Enter a name and description for your new calculator and click **Submit**.

        The new calculator is displayed on the Risk Calculator list.

        ![New risk calculator form](../image/v11newcalc2.png)

    4.  In the list, click the new calculator to create the conditions under which the calculator runs and specify the fields and values you want displayed on test result records and remediation tasks.

    5.  In the record that is displayed, click **New**.

    6.  Fill in out the fields in the tabs as appropriate.

        |Tab|Description|
        |---|-----------|
        |When this condition is met|Use the conditions builder to create the conditions under which the calculator runs. An example is: `Result is Failed or Result is Error`.|
        |Set these values|Use the template to select the fields and values you want displayed.|

    7.  Click **Submit**.

        The record is displayed with the new calculator rules and the group it belongs to.

2.  To reapply an existing calculator to test results or edit the rules and displayed values for an existing risk calculator, follow these steps.

    1.  From the Risk Calculators or Risk Rollup calculator lists, select the calculator you want to edit.

    2.  To reapply a risk calculator to your existing test result data from the record, click **Reapply Calculator**.

        All test results that meet the conditions of the calculator are updated.

        **Note:** Depending on the number of test results, this update may take time.

    3.  To edit the conditions and values, in the lower left in the Name column, click the calculator name.

        For risk calculators, the record and the **When this condition is met** and **Set these values** tabs are displayed.

    4.  Fill in the form as appropriate.

<table id="table_r3t_5bq_plb"><thead><tr><th>

Tab

</th><th>

Field Description

</th></tr></thead><tbody><tr><td>

When this condition is met

</td><td>

Use the filter conditions builder to create the conditions under which you want the calculator to run.

</td></tr><tr><td>

Set these values

</td><td>

Choose one to continue.-   Value type - Template. Choose fields from the list and corresponding values.
-   Script - Enter your changes using the editor.

**Note:** Editing script requires advanced knowledge of the ServiceNow AI Platform and the Configuration Compliance application.

</td></tr></tbody>
</table>3.  To apply the new rules on-demand to your existing test result data, follow these steps.

    1.  With the Risk Calculators list displayed, click a calculator you want to apply.

        The record is displayed.

    2.  Click **Reapply Calculator** to test and apply your changes on-demand to your import findings.

4.  View your changes on test results and continue to edit your calculators as required.



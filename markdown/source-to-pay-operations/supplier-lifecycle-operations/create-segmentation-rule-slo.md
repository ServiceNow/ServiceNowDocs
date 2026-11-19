---
title: Create segmentation rule
description: Create a segmentation rule that defines criteria for categorizing suppliers into different segments based on various attributes or performance factors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/source-to-pay-operations/supplier-lifecycle-operations/create-segmentation-rule-slo.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [SLO, Supplier Lifecycle Operations, segmentation rule, segmentation table, condition builder, categorizing suppliers, Supplier Relationship and Performance Management]
breadcrumb: [Configure Supplier Relationship and Performance Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Create segmentation rule

Create a segmentation rule that defines criteria for categorizing suppliers into different segments based on various attributes or performance factors.

## Before you begin

Role required: sn\_kpi.admin or sn\_slm.manager or sn\_slm.admin

## About this task

A segmentation rule groups onboarded suppliers into a segment so that you can apply the same KPIs to all of them. Set conditions on the rule to define which suppliers belong to the segment. Suppliers that match the conditions are automatically added to the segment and receive KPIs from the KPI templates that you map to the rule. You can also add individual suppliers manually.

When the rule runs, the system generates KPIs and KPI collection tasks for all the suppliers in the segment. For example, you can create one rule for all IT hardware suppliers to apply the same set of KPI templates to that group.

For more information, see [Add KPI templates to a segmentation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplier-lifecycle-operations/add-kpi-template-segmentation-rule.md), [Add suppliers to a segmentation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplier-lifecycle-operations/add-supplier-segmentation-rule.md), and [Run segmentation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplier-lifecycle-operations/run-segmentation-rule.md).

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Do one of the following:

    -   Under Quick actions, select **Create segmentation rule**.
    -   Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon.\), navigate to **Lists** &gt; **Relationship management** &gt; **Segmentation rules**, and then select **New**.
3.  On the form, fill in the fields.

<table id="table_k2y_2cw_1lc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Basic details

</td></tr><tr><td>

Name

</td><td>

Name of the segmentation rule.

</td></tr><tr><td>

Description

</td><td>

Brief description of the segmentation rule.

</td></tr><tr><td>

Active

</td><td>

Option that indicates the segmentation rule is active for use.

</td></tr><tr><td>

Owner

</td><td>

The person who owns the segmentation rule.

</td></tr><tr><td>

Frequency

</td><td>

The frequency at which the segmentation rule automatically runs. The available options are:-   Ad-hoc
-   Weekly
-   Monthly
-   Quarterly
-   Yearly


</td></tr><tr><td class="sub-head" colspan="2">

Conditions

</td></tr><tr><td>

Segmentation table

</td><td>

Extracts data from the specified table.

</td></tr><tr><td>

Condition

</td><td>

Conditions that define which suppliers belong to the segment. Select **Set conditions** to open the condition builder and add conditions with a field, operator, and value. For example, to select suppliers located in India, set the field to `Country`, the operator to `is`, and the value to `India`.After you set conditions, the link changes to **Edit conditions**.

</td></tr></tbody>
</table>4.  Select **Save**.


## Result

A new segmentation rule is created.

-   **[Add KPI templates to a segmentation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplier-lifecycle-operations/add-kpi-template-segmentation-rule.md)**  
Add KPI templates to a segmentation rule to define the KPIs that are generated for the suppliers in the segment when the rule runs. You must add at least one KPI template before you run the rule.
-   **[Add suppliers to a segmentation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplier-lifecycle-operations/add-supplier-segmentation-rule.md)**  
Add suppliers to a segmentation rule so that KPIs are generated for them when the rule runs.

**Parent Topic:**[Configure Supplier Relationship and Performance Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplier-lifecycle-operations/configuring-supplier-performance-mgmt.md)

**Related topics**  


[Add KPI templates to a segmentation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplier-lifecycle-operations/add-kpi-template-segmentation-rule.md)

[Add suppliers to a segmentation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/source-to-pay-operations/supplier-lifecycle-operations/add-supplier-segmentation-rule.md)


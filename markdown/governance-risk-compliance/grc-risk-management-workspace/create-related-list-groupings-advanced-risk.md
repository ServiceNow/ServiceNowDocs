---
title: Create related list groupings in Advanced Risk
description: Simplify the groupings of related lists on a record page and customize them to your specific needs, assigning meaningful names in the process. This configuration enhances readability and user experience when interacting with the forms.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Risk Management, Governance, Risk, and Compliance]
---

# Create related list groupings in Advanced Risk

Simplify the groupings of related lists on a record page and customize them to your specific needs, assigning meaningful names in the process. This configuration enhances readability and user experience when interacting with the forms.

## Before you begin

Role required: admin or sn\_grc\_workspace.record\_view\_admin

## About this task

On a form, there can be numerous related lists that can occasionally result in a cluttered view. To streamline the display, you have the option to select and configure the related lists you want to see on the form. By default, the ability to configure the related lists is given for the following tables:

-   Calculated Metric Definition table
-   Metric Definition table

While you can select any table and configure the related lists for that table, as an example, this procedure describes how you can create groupings for the Metric Definition table. Apart from the related lists, you can also specify a UX page that you want to display under a group.

## Procedure

1.  Navigate to **All** &gt; **Advanced Risk Assessment** &gt; **Administration** &gt; **Record View Configuration**.

2.  Select **Risk workspace configuration**.

3.  In the Table configurations related list, select **Metric Definition**.

4.  In the Group configurations related list, select **New**.

5.  On the form, fill in the fields.

<table id="table_bwh_s1s_zxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table configuration

</td><td>

Name of the table for which you're configuring the related list. This field is automatically set.

</td></tr><tr><td>

Name

</td><td>

Name of the group that is displayed on the related list of the form. For example, you can provide a name such as `Risk` for grouping risk-related objects, such as risks and risk statements.

</td></tr><tr><td>

Active

</td><td>

Option to indicate if the configuration is active.

</td></tr><tr><td>

Order

</td><td>

Order number of the group on the form. **Note:** If you want to display the order before the Details tab, then the order number must be less than or equal to `100`.

</td></tr><tr><td>

Condition

</td><td>

Conditions that must be met to be displayed on the form. For example, you can specify if a record is active, only then it must be displayed on the form.

</td></tr></tbody>
</table>6.  Select **Submit**.

7.  In the Group configurations related list, select the entry you created.

    1.  In the Group entries related list, select **New**.

    2.  On the form, fill in the fields.

<table id="table_zkr_hgc_b1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group configuration

</td><td>

Group for which the related list is created. For example, in this procedure, the group for which you're configuring the entry is **Risks**.

</td></tr><tr><td>

Order

</td><td>

Order of the entry on the UI page.

</td></tr><tr><td>

Application

</td><td>

Application for which the related list is being created. This field is automatically set to **GRC: Risk Management Workspace**.

</td></tr><tr><td>

Active

</td><td>

Option to indicate if the entry is active.

</td></tr><tr><td>

Type

</td><td>

Choice to indicate the type of item the group contains. The choices are as follows:-   **UX page**
-   **Related list**


</td></tr><tr><td>

Related list

</td><td>

Related list that you want must appear under the group. This option appears only when the **Type** field contains **Related list**.

</td></tr><tr><td>

Screen

</td><td>

Specific variation or version of a page. This option appears only when the **Type** field contains **UX page**.

</td></tr><tr><td>

Route

</td><td>

The path of the UX screen. This option appears only when the **Type** field contains **UX page**.

</td></tr></tbody>
</table>    3.  Select **Submit**.


## Result

The following figure shows grouped related lists.![How related lists are grouped on a form after configuration.](../image/related-list-groupings-advanced-risk.jpg)

**Parent Topic:**[Configuring Risk Management](../../grc-risk/concept/configure-risk-mgmt.md)


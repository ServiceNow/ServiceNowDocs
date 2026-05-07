---
title: Add view rules to workflow
description: Configure custom view rules to display specific fields, sections, or layouts for authorization packages using a particular workflow configuration. View rules enable workflow-specific user interfaces without modifying the base package form.
locale: en-US
release: australia
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workflow configuration, CAM workflow configuration, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Add view rules to workflow

Configure custom view rules to display specific fields, sections, or layouts for authorization packages using a particular workflow configuration. View rules enable workflow-specific user interfaces without modifying the base package form.

## Before you begin

Role required: sn\_irm\_cont\_auth.admin

## Procedure

1.  Navigate to **All** &gt; **Continuous Authorization and Monitoring** &gt; **Administration** &gt; **Workflow Configurations**.

2.  Select a workflow Configuration to add a view rule.

3.  To add a view rule, select **New** in the **View Rules** tab.

    ![New view rule.](../image/WF-view-rule1.png)

4.  In the **View Rule New record** form, fill in the following fields:

<table id="simpletable_vn3_vmj_thc"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter the name for the view rule.

</td></tr><tr><td>

Application

</td><td>

The default application scope is set.

</td></tr><tr><td>

Active

</td><td>

Select the **Active** option to enable the view rule.

</td></tr><tr><td>

Execution Order

</td><td>

-   Enter a number to define the view rule priority.
-   Lower numbers have higher priority \(evaluated first\). For example, enter 10 for high priority, 50 for medium, 100 for low.
-   By default the value is 100.


</td></tr><tr><td>

Experience Restricted

</td><td>

Select **Experience Restricted** option to restrict the view rule to CAM workspace.

</td></tr><tr><td>

Table

</td><td>

The table this view rule applies to. The default value is **Authorization Package \[sn\_irm\_cont\_auth\_auth\_pack\]**.

</td></tr><tr><td>

Advanced

</td><td>

Select **Advance** option to enable advanced configuration.Enable **Turn on ECMAScript 2021 \(ES12\) mode** to use JavaScript syntaxes and features for validation.

**Note:** If you select advanced option, then you can’t use the **Conditions** to define the view rule.

</td></tr><tr><td>

View

</td><td>

Select the search icon to select the view to which the view rule should apply.

</td></tr><tr><td>

Conditions

</td><td>

To add conditions that control when the view rule applies and to a specific role.

</td></tr><tr><td>

Form Settings

</td><td>

To configure the form display options.-   **Hide details &amp; UI actions**: Select to hide the form header actions
-   **Hide Journal Input Fields**: Select to hide activity stream input
-   **Hide section navigation**: Select to hide the navigation panel
-   **Disable section collapsing**: Select to avoid users from collapsing sections


</td></tr><tr><td>

Form Tabs

</td><td>

To configure which form tabs display.

</td></tr></tbody>
</table>    ![View rule fields.](../image/WF-view-rule2.png)

5.  Select **Submit** to add the new view rule.



---
title: Create a new state model attribute
description: Create custom state model attributes to add specialized capabilities to workflow steps.
locale: en-US
release: zurich
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2025-12-08"
reading_time_minutes: 1
breadcrumb: [GRC state model configuration, CAM workflow configuration, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Create a new state model attribute

Create custom state model attributes to add specialized capabilities to workflow steps.

## Before you begin

Role required: sn\_irm\_cont\_auth.admin

## Procedure

1.  Navigate to **All** &gt; **Continuous Authorization and Monitoring** &gt; **Administration** &gt; **GRC State Models**.

2.  Open the state model record that contains workflow states.

3.  On the **GRC workflow states** related list, select the workflow state for which you want to add a new state model attribute.

4.  On the selected workflow state record, select **State Model Attributes** tab.

5.  To add a new attribute, select **New**.

    ![Configuring state model attribute.](../image/WF-state-attributes1.png)

6.  On the **State Model Attribute New record** form, fill in the fields.

<table id="table_t53_xpz_thc"><thead><tr><th>

Fields

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Name for the attribute that appears in the lists. For example, Required approval.

</td></tr><tr><td>

Name

</td><td>

Name to identify the label in your instance. For example, required\_approval.

</td></tr><tr><td>

Description

</td><td>

Provides an explanation of what the attribute does. For example, Requires approval before proceeding to the next step.

</td></tr><tr><td>

Table name

</td><td>

Specifies which table this attribute applies to.**Note:** To configure the attribute to the authorization package, you must select **Authorization Package \[sn\_irm\_cont\_auth\_auth\_pack\]** in the table name drop-down.

</td></tr></tbody>
</table>    ![State model attribute fields.](../image/WF-state-attributes2.png)

7.  Select **Submit** to save the attribute.



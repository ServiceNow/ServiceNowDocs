---
title: Configure post-assessment actions
description: The post-assessment actions feature in Smart Assessment Engine enables you to automate actions based on assessment responses. The template designers can predefine actions using a rule engine, such as updating fields, creating follow-up assessments, or generating other records.
locale: en-US
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Post-assessment automations, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Configure post-assessment actions

The post-assessment actions feature in Smart Assessment Engine enables you to automate actions based on assessment responses. The template designers can predefine actions using a rule engine, such as updating fields, creating follow-up assessments, or generating other records.

## Before you begin

-   A subflow must be available and mapped to the assessment template category for which you want to configure post-assessment actions. For more information about how to create and build subflows, refer to Create a subflow in Workflow Studio and Building subflows.
-   To make actions available in post-assessment workflows, link the subflow to the appropriate template category. For more information, refer to [Link subflow to template category](link-subflow-to-action-set.md).
-   The Reusable Impact Framework plugin \(sn\_impact\_fwk\) and Post Assessment Actions for Smart Assessments plugin \(sn\_smart\_imp\_auto\) must be installed.

Role required: sn\_smart\_asmt.assessment\_admin or sn\_smart\_asmt.template\_manager and sn\_smart\_imp\_auto.automation\_creator

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace** to access the Assessment Workspace landing page.

2.  Create an assessment template or open an existing assessment template for which you want to configure post-assessment actions.

    Post-assessment actions can only be set on a published assessment template and remains in the Draft state until manually activated. After activated, post-assessment actions can’t be moved back to the Draft state while the template remains published. They can only be deactivated.

3.  Select the **Automations** tab.

4.  Select **Create Automation**.

5.  Provide a unique name and a description for the automation.

6.  Add either a conditional action set or a standalone action set.

<table id="choicetable_v2z_xht_42c"><thead><tr><th align="left" id="d276946e139">

Option

</th><th align="left" id="d276946e142">

Description

</th></tr></thead><tbody><tr><td id="d276946e148">

**Choose a conditional action set**

</td><td>

1.  Select **Add a conditional action set**.
2.  Select **If** and then select **+New condition set**.
3.  Create the conditional action set using the condition builder. For more information, refer to Condition builder.
4.  Select **Save**.
 **Note:** You can select **+New condition set** to add multiple conditions.

</td></tr><tr><td id="d276946e194">

**Choose a standalone action set**

</td><td>

Select **Add a standalone action set**.

</td></tr></tbody>
</table>7.  If the conditional action set is selected, to set condition select **If**.

8.  In the **Set actions** dialog box, fill in the fields as appropriate.

9.  If a standalone action set is selected, to set an action by selecting **then**.

10. Select an option for the **Action type** list.

    Based on the selected action type, new fields appear requiring additional details.

    The options displayed in the **Action type** field are subflows linked to the chosen template's categories. For more information on automated actions, see [Post-assessment automations](../concept/impact-automation.md).

    **Note:** Responses from dropdown, check box, radio, and attachment question types cannot be passed as action parameters because they are not supported.

11. Select **Activate**.

12. Acknowledge the **I understand the automation will no longer be editable** informational check box and then select **Activate**.

    The automation is now activated, and a confirmation message is displayed. When the assessor submits the assessment, the automation you set up is executed.


**Related topics**  


[bundle-cadev.flow-designer]


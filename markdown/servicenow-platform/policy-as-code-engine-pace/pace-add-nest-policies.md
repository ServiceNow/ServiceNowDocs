---
title: Add nested policies in a policy
description: Add existing policies to a policy's conditions to define the order a policy's execution and the conditions is executed.
locale: en-US
release: yokohama
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Passing parameters to PaCE policies, Administer PaCE policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Add nested policies in a policy

Add existing policies to a policy's conditions to define the order a policy's execution and the conditions is executed.

## Before you begin

**Note:** You must create a policy before adding it to another policy. For more information, see [Create a PaCE policy](pace-create-policy.md).

You can add a policy multiple times with different names and parameters. The policies must be configured and mapped to a document, and API variables and Config parameters may be required and mapped to be configured. For more information on how to add variables, see [Create a new variable for a policy version](pace-create-variable-policy-version.md).

Role required: sn\_pace.code\_editor

## Procedure

1.  Navigate to **Policies** &gt; **My Policies**.

2.  Select the policy you want to nest the policies in.

3.  In the **Data sources** section, select the **Policies** tab.

4.  Select **Add**.

5.  In the Add policy window, search and select the policy you want to add as a data source, then select **Next**.

6.  On the Details tab, enter the **Label** field and **Variable name** field and other configuration inputs as needed for the policy.

7.  In the Configure Inputs tab, under the Document section, select the value of the document type that depends on the integration for the policy.![Input document config tab.](../image/pace-config-inputs-tab.jpg)

8.  Pick a variable to pass for in the API variable and Config parameter sections you created in the beginning of this task.

    **Note:** You can specify the value in the fields as needed.

9.  Select **Save**.

    ![Policies tab.](../image/pace-data-source-policies.jpg)


## Result

The policies now appear on the Policies tab and can be added in the condition section or the Then section of the Policy builder. For more information on how to add the policies in the builder, see [Policy logic condition fields](../reference/pace-policy-logic-fields.md).


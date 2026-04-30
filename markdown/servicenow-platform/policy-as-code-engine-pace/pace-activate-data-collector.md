---
title: Activate and build data collectors
description: Activate and build data collectors to add to a policy.
locale: en-US
release: xanadu
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Passing parameters to PaCE policies, Administer PaCE policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Activate and build data collectors

Activate and build data collectors to add to a policy.

## Before you begin

Role required: sn\_pace.code\_editor

## Procedure

1.  Select the **Versions** tab, then the data collector draft name.

2.  Select the **Build** tab.

3.  In the Data sources section, select the variable tab you want to define.

    1.  Click **Add**.

        ![Add new input/output](../image/pace-add-new-input.jpg)

    2.  On the Add new input form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Label|\(Optional\) Label of the input or output.|
        |Name|Enter a name of the input or output.|
        |Type|Select the type of the input or output.|
        |Mandatory|Select this check box if the input is mandatory.|
        |Description|Description of the input or output.|
        |Default value|Specify a default value.|

        **Note:** Inputs are used as parameters that help collect the correct data to be used in the policy. Outputs are used to specify output variables that can be used in the policy logic.

    3.  Click **Save**.
    4.  Repeat the steps to create the inputs and outputs as needed.
4.  Enter your inputs or outputs and write your code in the Data collector script, as needed.

5.  Add an exception error in your data collector by entering the following script: `throw new PaCEExecutionError`.

    When you execute the policy with the data collector exception, the error message will appear under the Output tab in the Execution errors section.

6.  Click **Save**.

7.  When you're finished, select **Publish**.

8.  In the Publish draft window, select the **Activate this data collector** check box, then **Publish**.

    **Note:** When the data collector has been activated, you will be unable to make changes to the inputs or outputs.


